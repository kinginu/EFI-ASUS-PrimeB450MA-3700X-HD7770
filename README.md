# ASUS Prime B450M-A + Ryzen7 3700X + Radeon HD7770

**Latest working macOS**: 12.6
<br>
**Current OpenCore**: 0.8.5-DEGUB

## Complete hardware specs
- Ryzen7 3700X
- ASUS PrimeB450M-A (BTO MOUSE computer HM-AB450)
- Radeon HD7770 2GB
- 16Gb DDR4 2666Mhz
- Wifi/BT Intel AX200

## What works
- macOS Monterey
- Audio
- HDMI/DP
- Wifi/BT
- Shutdown/Reboot

## What doesn't work
- Sleep

## Kexts used:
- [Lilu.kext](https://github.com/acidanthera/Lilu/releases)  
-- must have to boot
- [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases)  
-- must have to boot
- [WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)  
-- for graphics
- [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases)  
-- for audio
- [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases)  
-- for Ethernet
- [BlueToolFixup](https://github.com/acidanthera/BrcmPatchRAM/releases)  
-- for non-native Bluetooth card
- [Airportitlwm](https://github.com/OpenIntelWireless/itlwm/releases)  
-- 
- [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases)  
-- 
- [AMDRyzenCPUPowerManagemaent](https://github.com/trulyspinach/SMCAMDProcessor)  
-- CPU power management for Ryzen
- [AppleMCEReporterDisabler](https://github.com/acidanthera/bugtracker/files/3703498/AppleMCEReporterDisabler.kext.zip)  
-- 

## To use this EFI
- I deleted information about Serial, Board Serial, SmUUID, and Apple ROM. If you use this EFI, please use GenSMBIOS and generate required information.
- [SMBIOS](https://github.com/corpnewt/GenSMBIOS)
- [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/config.plist/#creating-your-config-plist)

## Radeon HD7000 Series Issue
- OpenCore is designed for UEFI systems, but the HD7000 series does not support Graphics Output Protocol (GOP), so it is not UEFI bootable. UEFI booting is possible by rewriting the BIOS of the graphics card to one that supports GOP. Do this at your own risk!
[This](https://winraid.level1techs.com/t/amd-and-nvidia-gop-update-no-requests-diy/30917) is link for GOP_Updater.

## Thanks/Credits
- [Opencore Team](https://dortania.github.io/getting-started/)
- [lordkag](https://winraid.level1techs.com/u/lordkag)  
for GOP_Updater
