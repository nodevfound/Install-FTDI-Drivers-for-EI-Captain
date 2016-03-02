# Install-FTDI-Drivers-for-EI-Captain for TIAO 

Download Driver at http://www.ftdichip.com/Drivers/VCP.htm
The installation location is at /Library/Extensions/FTDIUSBSerialDriver.kext

Addtional Notes at FTDI Site, but it does not work for the EI-CAPTAIN:
http://www.ftdichip.com/Support/Documents/AppNotes/AN_134_FTDI_Drivers_Installation_Guide_for_MAC_OSX.pdf

The following disable the system intergrity protection to load unsigned kext module <br>
https://developer.apple.com/library/mac/documentation/Security/Conceptual/System_Integrity_Protection_Guide/ConfiguringSystemIntegrityProtection/ConfiguringSystemIntegrityProtection.html#//apple_ref/doc/uid/TP40016462-CH5-SW1

Added the following at /Library/Extensions/FTDIUSBSerialDriver.kext/Contents/Info.plist
 
