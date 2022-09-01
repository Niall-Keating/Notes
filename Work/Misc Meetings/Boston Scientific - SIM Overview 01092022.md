---
date: 01-09-2022
type: meeting notes
tags: [Boston-Scientific, BSCI, Vodafone, AT&T, Verizon, Teal, Twilio, Kore, Kore-Wireless, eSIM, eUICC, MNO, MVNO, Cellular, CAT1, CATM, MFF2, Thales, GSMA. Multi-IMSI, Jasper, M2M, GDSP, Remote-Provisioning,]
location: Microsoft Teams
---

## Attendees
- Tomas O'Mahonney (Taoglas)
- Adrian Burns (Taoglas)
- Niall Keating (Taoglas)
- Derek Browne (Taoglas)
- Neil (Boston Scientific)
- Robert (Boston Scientific)

## Notes
- Adrian presented - [[(BSCI)(01092022) - Taoglas IoT Solutions - Connectivity Options.pdf]]
	- Gave an overview of the different SIM types.
		- 2FF - Mini SIM
		- 3FF - Micro SIM
		- 4FF - Nano SIM
		- MFF2- Chip SIM
			- Also known as:
				- eSIM
				- Soldered SIM
	- **Misconception** - Only MFF2 SIMs can be an eSIM
		- This is incorrect, eSIM's are much much more than a hardware SIM that can be soldered onto a PCB
		- It's an entire set of tools that allows for multiple SIM profiles, remote provisioning, OTA updates
		- eSIMs have a very lite operating system on them to marshal profiles and updates
	- Updates to the eSIM happen via a link directly to the modem/module, no interaction with host CPU(i.e. ESP32 on the Lynx) required.

## More Info