---
project: Teva
date: 22-08-2022
type: internal meeting
tags: [Ethernet-Gateway, Custom-Domains]
---
# Chat with Kamil 30/08/2022

## A


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

