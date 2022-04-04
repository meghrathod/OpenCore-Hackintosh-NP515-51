# macOS on Acer Nitro 5 Spin(NP515-51)


![Nitro 5 Spin](https://img.shields.io/badge/Acer%20Nitro%205%20Spin-NP515--51-red)
[![MacOS Monterey](https://img.shields.io/badge/Monterey-12.0-purple.svg)](https://www.apple.com/macos/monterey-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.7.1-blue.svg)](https://github.com/acidanthera/OpenCorePkg/releases/latest)


## READ THE ENTIRE README.MD BEFORE YOU START

### I am not responsible for any damages you may cause

- I will try my best to keep the repo updated with the latest kexts and OpenCore version.
- This EFI is configured for macOS Monterey, may or may not work for lower versions.
- With every EFI update you retrieve from here please remember to go through the post install guide.


## Summary

#### Video and Audio

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Full Graphics Accleration (QE/CI)    | ✅   | `WhateverGreen.kext` and `Lilu.kext`  |
| Audio Recording                      | ✅   | `AppleALC.kext` with Layout ID = 3 and `SSDT-HPET.aml`   |
| Audio Playback                       | ✅   | `AppleALC.kext` with Layout ID = 3 and `SSDT-HPET.aml`   |
| Automatic Headphone Output Switching | ✅   | `AppleALC.kext` with Layout ID = 3 and `SSDT-HPET.aml`   |
| Dock Audio Port                      | ✅   | `AppleALC.kext` with Layout ID = 3 and `SSDT-HPET.aml`   |

#### Power, Charge, Sleep and Hibernation

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Battery Percentage Indication        | ✅   | `SMCBatteryManager.kext`            | 
| S3 Sleep/ Hibernation Mode 3         | ✅   | Used Hackintool for the same |  |   
| Battery Life                         | ✅   | Native, comparable to Windows/Linux. |

#### Input/ Output

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Bluetooth                            | ✅   | `BlueToolFixup.kext`  |
| Ethernet                             | ✅   | Native support from type-C port  |
| USB Power Properties in macOS        | ✅   | `SSDT-EC-USBX.aml` |

#### Display, TrackPad, TrackPoint, and Keyboard

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Brightness Adjustments | ✅  | `WhateverGreen.kext`, `SSDT-PNLF.aml` and `BrightnessKeys.kext`|
| Touchscreen            | ✅  | `VoodooPS2Controller.kext` |
| TrackPad               | ✅  | `VoodooPS2Controller.kext` |
| Built-in Keyboard      | ✅  | `VoodooPS2Controller.kext` |
| Multimedia Keys        | ✅  | `BrightnessKeys.kext` |

#### Apple Features

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| iCloud, iMessage, FaceTime           | ✅   | Whitelisted Apple ID, Valid SMBIOS  |
| Time Machine                         | ✅   | Native  |


#### Non-Fuctional

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| WiFi                                 | ❌    | Qualcomm Wifi card has to be replaced  |
| Fingerprint Reader                   | ❌    | macOS doesn't support non-native Touch ID |
| AirDrop, Continuity and Handoff      | ❌    | Non-native Wifi Card  |
| Nvidia GTX 1050 4GB                  | ❌    | Unsupported by macOS Monterey  |


## References

Read these before you start:

- [dortania's Hackintosh guides](https://github.com/dortania).
- [dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/).
- [dortania's OpenCore Post Install Guide](https://dortania.github.io/OpenCore-Post-Install/).
- [dortania/ Getting Started with ACPI](https://dortania.github.io/Getting-Started-With-ACPI/).
- [dortania/ opencore `multiboot`](https://github.com/dortania/OpenCore-Multiboot).
- [dortania/ `USB map` guide](https://dortania.github.io/OpenCore-Post-Install/usb/).
- [WhateverGreen Intel HD Manual](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.IntelHD.en.md).
- `Configuration.pdf` and `Differences.pdf` in each `OpenCore` releases.


## Requirements 

- A macOS machine(optional): to create the macOS installer.
- Flash drive, 12GB or more, for the above purpose.  
- [ProperTree](https://github.com/corpnewt/ProperTree) if you need to edit plist files on Windows.  
- [MountEFI](https://github.com/corpnewt/MountEFI) to quickly mount EFI partitions.  
- [IORegistryExplorer](https://developer.apple.com/downloads), for diagnosis.  
- [Hackintool](https://www.insanelymac.com/forum/topic/335018-hackintool-v286/), for diagnostic ONLY, Hackintool should not be used for patching, it is outdated.
- Patience and time, especially if this is your first time Hackintosh-ing.

## Hardware 

| Category  | Nitro 5 Spin NP515-51         |            
| --------- | ------------------------------| 
| CPU       | Intel Core i5-8250-U          | 
| SSD       | Samsung 970 Evo Plus 500GB    | 
| Display   | 15.6' IPS FHD (1920x1080)     | 
| WiFi & BT | Qualcomm Atheros QCA61x4A     | 
| iGPU      | Intel UHD 620                 |

## How to get started 

Before you do anything, please familiarize yourself with basic Hackintosh terminologies and the basic Hackintosh process by throughly reading Dortania guides as linked in `REFERENCES`

- Creating a macOS installer: refer to [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- [**README-HARDWARE**](/Other/README_HARDWARE.md): Requirements before installing.
- [**README-OTHERS**](/Other/README_OTHERS.md): for post installation settings and other remarks.


### CREDITS 
- [Apple](https://www.apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for all the kexts/utilities that they made.
- [Rehabman](https://github.com/RehabMan) and [Daliansky](https://github.com/daliansky) for the patches and guides and kexts.
- [Dortania](https://github.com/dortania) for for the OpenCore Install Guide.

