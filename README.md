# Steps to Install-FTDI-Drivers-for-EI-Captain for TIAO 

Issue: Not able to load unsigned kext kernel module for FTDI driver, the following steps disable the OSX system intergrity protection to load the FTDI driver. It is not safe and not a long term solution. 

1) Download Driver at http://www.ftdichip.com/Drivers/VCP.htm
The installation location is at /Library/Extensions/FTDIUSBSerialDriver.kext

2) Added the following at /Library/Extensions/FTDIUSBSerialDriver.kext/Contents/Info.plist, refer to additional_field.txt

3) The following disable the system intergrity protection to load unsigned kext module <br>
https://developer.apple.com/library/mac/documentation/Security/Conceptual/System_Integrity_Protection_Guide/ConfiguringSystemIntegrityProtection/ConfiguringSystemIntegrityProtection.html#//apple_ref/doc/uid/TP40016462-CH5-SW1

4) sudo kextload /System/Library/Extensions/FTDIUSBSerialDriver.kext/ <br>

***To Note***:<br>
Addtional Notes at FTDI Site, but it does not work for the EI-Captain:
http://www.ftdichip.com/Support/Documents/AppNotes/AN_134_FTDI_Drivers_Installation_Guide_for_MAC_OSX.pdf

***Useful Links***<br>
http://www.mommosoft.com/blog/2014/10/24/ftdi-chip-and-os-x-10-10/<br>
http://www.tiaowiki.com/forums/index.php?topic=4334.0<br>

***Useful Commands***<br>
1) sudo kextunload /System/Library/Extensions/FTDIUSBSerialDriver.kext/ <br>
2) sudo kextload /System/Library/Extensions/FTDIUSBSerialDriver.kext/ <br>
3) csrutil status <br>
4) nvram -xp<br>
5) kextstat <br>

