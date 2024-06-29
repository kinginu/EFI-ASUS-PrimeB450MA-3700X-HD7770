# Hackintosh ASUS Prime B450M-A + Radeon HD7770
OpenCore Hackintosh settings for ASUS Prime B450M-A with Ryzen7 3700X and Radeon HD7770

**Latest working macOS**: macOS Monterey 12.6  
**Current OpenCore**: 0.8.5-DEBUG

## Hardware
- **Motherboard**: ASUS Prime B450M-A (BTO MOUSE computer HM-AB450)
- **CPU**: Ryzen7 3700X
- **GPU**: Radeon HD7770 2GB
- **RAM**: 16GB DDR4 2666MHz
- **WiFi/BT**: Intel AX200

## Radeon HD7000 Series Issue
- OpenCore is designed for UEFI systems, but the HD7000 series does not support Graphics Output Protocol (GOP), making it not UEFI bootable. However, UEFI booting is possible by flashing the BIOS of the graphics card to one that supports GOP. Please proceed at your own risk! For more information, you can refer to [this post](https://winraid.level1techs.com/t/amd-and-nvidia-gop-update-no-requests-diy/30917).

## What Works
- macOS Monterey
- Audio
- HDMI / DP
- Wifi / Bluetooth
- Shutdown / Reboot

## What Doesn't Work
- Sleep

## Kexts Used
| Kext | Version | Notes |
| --- | --- | --- |
| [Lilu.kext](https://github.com/acidanthera/Lilu/releases) | - | Must have to boot |
| [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | - | Must have to boot |
| [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | - | For graphics |
| [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | - | For audio |
| [RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) | - | For Ethernet |
| [BlueToolFixup.kext](https://github.com/acidanthera/BrcmPatchRAM/releases) | - | For non-native Bluetooth card |
| [Airportitlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) | - | For Intel WiFi |
| [IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | - | For Intel Bluetooth |
| [AMDRyzenCPUPowerManagement.kext](https://github.com/trulyspinach/SMCAMDProcessor) | - | CPU power management for Ryzen |
| [AppleMCEReporterDisabler.kext](https://github.com/acidanthera/bugtracker/files/3703498/AppleMCEReporterDisabler.kext.zip) | - | Disables Apple MCE Reporter |


## To Use this EFI
- Serial, Board Serial, SmUUID, and Apple ROM are deleted. Generate them using GenSMBIOS. 
[SMBIOS](https://github.com/corpnewt/GenSMBIOS) [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/config.plist/#creating-your-config-plist)

## Thanks / Credits
- [Opencore Team](https://dortania.github.io/getting-started/)
- [lordkag](https://winraid.level1techs.com/u/lordkag) for the GOP Updater
