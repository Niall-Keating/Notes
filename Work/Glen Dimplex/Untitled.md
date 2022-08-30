chat with kamil


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


during device in