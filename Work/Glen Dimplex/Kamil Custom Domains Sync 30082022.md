---
project: Glen Dimplex
date: 30-08-2022
type: internal meeting
tags: [GD, Ethernet-Gateway, Custom-Domains]
---
# Chat with Kamil 30/08/2022

## Attendees
- Niall Keating
- Kamil Gardziejczyk

## Notes

- In the factory, we use a script called `AES_BOOTLOADER.pl` to flash the bootloader and application binary to the boards. 
	- This was originally provided by Microchip and can be used to flash most of their ARM absed devices
	- We made some modifications that allow us to pass through some more info to the device during provisioning. 
		- i.e. Discovery Service URL, HealthCheck URL, BLE Pin etc.
		- This works as follows:
			- perl script -> usb -> bootloader -> special area of flash 
			- Look at the linker file for the special area of flash called DeviceInfo (256Bytes)
		- Basically the perl scrip flashes the bootlaoder, then communicates with the bootlaoder to send it the above details, the bootlaoder then stores these in a section of flash.
- In production firmware, this section of flash is read during device boot to ascertain the Azure URLS to use
	- This needs to be extended to include the new custom URLs
		- These need to be added at the end of the block of flash so as not to cause backward compatability issues with in the firmware that does/doesn't ahve these URLs.
- Similar to on our EDGE4 based devices, there's two build modes:
	1. App Flash
		- For dev builds
	2. Bootloader Flash
		- For production builds
- When we boot the following is called:

``` C

void PrepareDeviceInfo(void) {
   memcpy(&GDIDAndToken[0], &deviceInfo[0], GDID_TOKEN_SIZE);
   memcpy(&mutualAuthenticationEnabled, &deviceInfo[MUTUAL_AUTH_OFFSET], 1);
#ifndef FW_PRODUCTION_MODE
   memcpy(&discoveryServiceCustomURL[0], &deviceInfo[DISCOVERY_CUSTOM_SERVICE_URL_OFFSET], DISCOVERY_CUSTOM_SERVICE_URL_LENGTH);
   memcpy(&discoveryServiceURL[0], &deviceInfo[DISCOVERY_SERVICE_URL_OFFSET], DISCOVERY_SERVICE_URL_LENGTH);
   memcpy(&healthCheckURL[0], &deviceInfo[HEALTH_CHECK_URL_OFFSET], HEALTH_CHECK_URL_LENGTH);
   memcpy(&healthCheckCustomURL[0], &deviceInfo[HEALTH_CHECK_CUSTOM_URL_OFFSET], HEALTH_CHECK_CUSTOM_URL_LENGTH);
#endif
   ble_passkey = (deviceInfo[BLE_PASSKEY_OFFSET] << 24) | (deviceInfo[BLE_PASSKEY_OFFSET + 1] << 16) | (deviceInfo[BLE_PASSKEY_OFFSET + 2] << 8) | (deviceInfo[BLE_PASSKEY_OFFSET + 3] << 0);
   memcpy(&slot0FileName[0], &deviceInfo[SLOT0_NAME_OFFSET], SLOT_NAME_LENGTH);
   memcpy(&slot1FileName[0], &deviceInfo[SLOT1_NAME_OFFSET], SLOT_NAME_LENGTH);
   memcpy(&slot2FileName[0], &deviceInfo[SLOT2_NAME_OFFSET], SLOT_NAME_LENGTH);
}

```

- This checks if we are in production firmware mode, if we are it doesn't use the flash URLs for some reason, this was news to Kamil, he only realised as I was on the call with him. 
	- He thought that this should be the inverse
- The URLs sit in RAM when not stored in flash.
- Regardless, this will impact UAT testing, this needs to be fixed before handing over to GD.
- He is planning to work on this today.


