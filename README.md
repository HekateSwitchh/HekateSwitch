# hekate - Nyx

Custom Graphical Nintendo Switch bootloader, firmware patcher, tools, and more.

- [Features](#features)  
- [Bootloader folders and files](#bootloader-folders-and-files)  
- [Bootloader configuration](#bootloader-configuration)  
  * [hekate global Configuration keys/values](#hekate-global-configuration-keysvalues-when-entry-is-config)  
  * [Boot entry key/value combinations](#boot-entry-keyvalue-combinations)  
  * [Boot entry key/value combinations for Exosphère](#boot-entry-keyvalue-combinations-for-exosphère)  
  * [Payload storage](#payload-storage)  
  * [Nyx Configuration keys/values](#nyx-configuration-keysvalues-nyxini)  

---

## Features

- **Fully Configurable and Graphical** with Touchscreen and Joycon input support  
- **Launcher Style, Background and Color Themes**  
- **HOS (Switch OS) Bootloader** — For CFW Sys/Emu, OFW Sys and Stock Sys  
- **Android & Linux Bootloader**  
- **Payload Launcher**  
- **eMMC/emuMMC Backup/Restore Tools**  
- **SD Card Partition Manager** — Prepares and formats SD Card for HOS, Android, and Linux  
- **emuMMC Creation & Manager** — Supports migration and repair of existing emuMMC  
- **Switch Android & Linux flasher**  
- **USB Mass Storage (UMS) for SD/eMMC/emuMMC** — Converts Switch into a mass storage device  
- **USB Gamepad** — Converts Switch with Joycon into a USB HID Gamepad  
- **Hardware and Peripherals info** (SoC, Fuses, RAM, Display, Touch, eMMC, SD, Battery, PSU, Charger)  
- **Additional Utilities** including Archive Bit Fixer, Touch Calibration, Benchmarking, AutoRCM, and more  

---

## Bootloader folders and files

| Folder/File              | Description                                                           |
| ------------------------ | --------------------------------------------------------------------- |
| bootloader               | Main folder.                                                          |
|  \|__ bootlogo.bmp       | Used if no `logopath` key is found. Optional.                         |
|  \|__ hekate_ipl.ini     | Main bootloader configuration and boot entries.                       |
|  \|__ nyx.ini            | Nyx GUI configuration.                                                |
|  \|__ patches.ini        | External patches.                                                     |
|  \|__ update.bin         | Automatically updated binary for modchip usage.                       |
| bootloader/ini/          | Individual configuration files.                                       |
| bootloader/res/          | Nyx resources (icons, backgrounds).                                   |
| bootloader/sys/          | System modules for hekate and Nyx.                                    |
| bootloader/screenshots/  | Stores screenshots taken in Nyx.                                      |
| bootloader/payloads/     | Payload storage for custom firmware, Linux, or tools.                 |

---

## Bootloader configuration

The bootloader can be configured via `bootloader/hekate_ipl.ini`. Each `.ini` section represents a boot entry, except `[config]` which defines global parameters.  

- Global configuration supports keys such as `autoboot`, `bootwait`, `autohosoff`, and others.  
- Boot entries support definitions for kernel replacement, payload launching, emuMMC pathing, RAM overclocking, and more.  

---

## Payload storage

Hekate includes an internal payload storage system, enabling configuration and execution of payloads outside of the BPMP environment.  

Key capabilities include:  
- Support for forced autoboot and menu overrides  
- Payload execution from specified storage locations  
- Integration with emuMMC pathing and ID-based entry booting  

---

## Nyx Configuration keys/values (nyx.ini)

Nyx allows additional customization via `nyx.ini`:  

- **themebg**: Background color  
- **themecolor**: Highlight color  
- **entries5col**: Column layout for entries  
- **verification**: Backup/restore verification mode  
- **jcdisable**: Joycon driver enable/disable  
- **bpmpclock**: Clock performance configuration  

---

## Website  

For downloads, documentation, and updates, visit:  
👉 [hekateswitch.com](https://hekateswitch.com)  

---

## License  

This project is released as open source. Redistribution and modification are permitted under the applicable license included with the source.  

