# Hackintosh-MSI-Z690-EDGE-WIFI-DDR4_i7-13700K_RX580

This is an OpenCore version of MSI Z690 EDGE WIFI DDR4 Hackintosh EFI. It works on macOS Vetura & Sonoma.

## Notes
The SMBIOS to be set to MacPro7,1 (now preset, please modify it after the installation is completed).
This config defaults to no verbose mode. To enable verbose mode, config.plist needs to modify the following item: NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args, add -v.
The config startup disk policy ScanPolicy value is set to 0. Can boot Windows or Other OS (Linux, Unix). If you need to specify the search partition type, please refer to the OC configuration manual.
This config defaults to not displaying the OC Picker menu. If you want to turn on the menu display, set it as follows: Misc-Boot-ShowPicker value is true (YES in the plist editor).
UTBMap.kext was customized for me based on the motherboard wiring. If you encounter USB-related errors, you can customize UTBMap yourself, or cancel loading the kext and change the XhciPortLimit value to true.

## Hardware
| Item | Brand | Model | Driver | Comment |
|-----|-----|-----|-----|-----|
| Motherboard | MSI | MPG Z690 EDGE WIFI DDR4 | | |
| CPU | Intel | i7-13700K | | |
| RAM | Corsair | Vengeance LPX 32GB (4x8GB) DDR4 DRAM 3200MHz | | |
| iGPU | Intel | UHD Graphics 770 | built-in | Headless mode |
| dGPU | MSI | RX 580 Armor 4GB | built-in | 2304 SP |
| SSD | Samsung | 980 PRO 1TB PCIe NVMe Gen4 | | |
| WiFi/Bluetooth | Fenvi | T919 Wi-Fi 2.4/5GHz and Bluetooth 4.0 PCI-E Card | built-in | |
| Ethernet | Intel | I225-V | [AppleIntelI210Ethernet.kext] | |
| Audio | Realtek | ALC897 | [AppleALC](https://github.com/acidanthera/AppleALC) | |
| PSU | EVGA | SuperNOVA 650 G1 | | |
| Case | inWin | 303 | | |
| Monitor | Benq | VZ2470 | | |

 

## BIOS Setup
| Name | Option |
| --- | --- |
| SR-IOV Support | Enabled |
| CFG Lock | Disabled |
| iGPU-Multi-Monitor | Disabled |
| Fast Boot | Disabled |
| Secure Boot | Disabled |
| DTM | Enabled |
| TPM 2.0 | Disabled |

## :white_check_mark: Working:

- [x] CPU power management.
- [x] Graphics acceleration.
- [x] Keyboard & trackpad with all macOS gestures.
- [x] Wi-Fi.
- [x] Bluetooth.
- [x] USB ports.
- [x] HDMI video & audio output.
- [x] Ethernet.
- [x] Audio (Internal speakers, 3.5mm headphone jack).
- [x] Internal microphone.
- [x] VGA WebCam.
- [x] AirDrop & Handoff & AirPlay & Screen Mirroring.
- [x] iCloud & App Store.
- [x] iMessage & FaceTime.

## :closed_lock_with_key: SMBIOS 

You will need to generate your own SMBIOS and configure, you can use the following SMBIOS: MacPro7,1.

Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate your own unique SMBIOS and then copy each parametter following path (recomended to follow the guide above):
  - Config.plist -> PlatformInfo -> Generic

## Credits:

[**Apple**](http://apple.com/)

[**Acidanthera**](https://github.com/acidanthera)

[**Dortania**](https://dortania.github.io/getting-started/)
