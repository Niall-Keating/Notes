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
- 



problem is in the factory we have aes bootloader perl script
	Originalkly this was from microsoft, tool to flasjh bootlaoder and binary onto same70
	we made some mods so that we can poass more in to thedevice duting flashing
	ie discovery serviuce url, healthcheck ble pin number etc...
	bootloaader puts special cvalues in flash 

perl script -> usb -> bootloader -> special area of flash (look at linker (Device Info) 256Bytes

flash mode 
	development
bootlaoder mode
	production

when we boot 
	PrepareDeviceInfo()

Only in booaltader mode

in flashmode it sits in ram


during device initialisination we check ioif in production mode
	copy from flash into (fw_common.c(prepareDeviceInfo()))

It looks like in firmare it doesn't use urls from flash in production mode 

Looks like will use urls hardcoded from binary 


He needs to put urls in end of flash section

This needs to be fixed before sendiong over to them

He's hoping he can do them today 


