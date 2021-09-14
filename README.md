# BIGTREETECH SKR E3 Turbo for Creality CR10 Mini with a EZABLPro-like bed-leveling sensor (capacitive)
**_This is a fork of the original repo of the BTT for the SKR E3 Turbo: [bigtreetech/BIGTREETECH-SKR-E3-Turbo](https://github.com/bigtreetech/BIGTREETECH-SKR-E3-Turbo)_**
---
My most important changes on top of the original repo are for:
- Creality CR10 Mini printer
  - Bed size: 300 x 220mm
  - Z_MAX: 300mm 
  - PID values and various minor adjustments
- Custom changes:
  - use the chamber sensor to measure temperature inside the case
  - inverted the endstop for Z to work with my bed levelling sensor ([LJC18A3-B-Z/BX](https://www.amazon.de/gp/product/B072C35ZDC/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1))
  - activated the TMC driver for the Z2 motor (using the E1) because I have a upgraded my printer to dual-Z motors
  - changed motor currents:
    - X_CURRENT       650
    - Y_CURRENT       800 (the bed is heavier than the X axis)
    - Z_CURRENT       650
    - Z2_CURRENT      650
 ---

BIGTREETECH SKR E3 Turbo (V1.x) is the next mainboard in the BTT SKR Mini E3 series of ultra-quiet, low-power, high-quality 3D printing machine controller boards from BIQU.

These and other SRK mainboard/motherboard for 3D-printers are produced by the 3D printing team of Shenzhen Bigtree Technology Co., Ltd. 

The first BIGTREETECH SKR Mini E3 V1.x 32-bit control boards with integrated TMC stepper-drivers was initially specially designed to be a drop-in replacement upgrade board for the Ender 3 printers by Creality, making replacing the original 8-bit mainboard/motherboard hardware used by the very popular Ender-3 3D-printer quick and easy for most users. Software updates have since released also added compatibility for other 3D-printers with a single Z-axis stepping-motor, including support for CR-10, CR-10 Mini, Ender 3 Pro from Creality.

BIGTREETECH SKR Mini E3 V2.x has added additional hardware improvements and enhancements based on community feedback. Among other things, these improvements and enhancements with SKR Mini E3 V2.x include two Z-axis interface ports, and SKR Mini E3 V2.x plus BIGTREETECH SKR E3 Turbo is today, in addition to the 3D-printers already support by the SKR Mini E3 V1.x boards, also compatible with CR-10S, CR-10 S4, CR-10 S5, Ender 5, Ender 5 Pro, and Ender 5 Plus 3D-printers from Creality.

BIGTREETECH SKR E3 Turbo uses the more powerful MCU, nerwer stepper drivers and has a slightly larger footprint for dual extruders/hotends or independent dual Z depending on firmware configuration.

BIGTREETECH SKR E3 Turbo (V1.x) features:

- 120MHz LPC1769 MCU
- 5 x integrated TMC2209s with Trinamic's Low Power Standby feature* and sensorless homing
- Onboard EEPROM
- 4-layer PCB
- USB port ESD protection via USBLC6-2 diode
- Onboard dual z connectors when using a single Z driver or independent dual Z when repurposing the second extruder driver
- Neopixel support (without needing to mod Marlin/change to third-party libraries)
- TFT support
- Dedicated probe port
- Powerloss detection via external module
- Dual, independently controlled, fan headers
- Power supply control via external module
- Dual extruder filament runout detection
- Onboard thermistor (currently disabled in Marlin configuration example as Marlin Firmware does not yet have an "board sensor" feature)

Pre-tested Marlin Firmware configuration example files for these 3D-printers with stock is available in an upstream repository here:

- https://github.com/MarlinFirmware/Configurations/

Marlin config examples for Creality Ender-3, Ender-5, Ender-5 Pro, and CR-10S:

- https://github.com/MarlinFirmware/Configurations/tree/import-2.0.x/config/examples/Creality/Ender-3/BigTreeTech%20SKR%20E3%20Turbo
- https://github.com/MarlinFirmware/Configurations/tree/import-2.0.x/config/examples/Creality/Ender-5/BigTreeTech%20SKR%20E3%20Turbo
  - https://github.com/MarlinFirmware/Configurations/tree/import-2.0.x/config/examples/Creality/Ender-5/BigTreeTech%20SKR%20E3%20Turbo%20with%20BLTouch
- https://github.com/MarlinFirmware/Configurations/tree/import-2.0.x/config/examples/Creality/Ender-5%20Pro/BigTreeTech%20SKR%20E3%20Turbo
  - https://github.com/MarlinFirmware/Configurations/tree/import-2.0.x/config/examples/Creality/Ender-5%20Pro/BigTreeTech%20SKR%20E3%20Turbo%20with%20BLTouch
- https://github.com/MarlinFirmware/Configurations/tree/import-2.0.x/config/examples/Creality/CR-10S/BigTreeTech%20SKR%201.4%20Turbo%20TMC2209

Note! After refreshing the new firmware, please always restore defaults first and then store settings, the new coordinates used for levelling will take effect, LCD option path: Configuration-> Restore defaults, Configuration-> Store settings.

Disclaimer! Marlin firmware needs to be configured and customized by the customer themselves, the reason for this is that BIQU / BIGTREETECH does not know the specific hardware configuration of each individual customer and can therefore not support individual configuration of special firmware specific to each customer. BIQU customer service will however if contacted provide configuration suggestions if details on your specific hardware setup are described. Other than e-mailing to <support@bigtree-tech.com> it is recommended to also use the BigTreeTech Facebook group and BigTreeTech Subreddit (Reddit community) channels for support, as well as posting bug-reports and feature-request as "issues" on @bigtreetech GitHub repository for BIGTREETECH-SKR-E3-Turbo:

- https://github.com/bigtreetech/BIGTREETECH-SKR-E3-Turbo/issues
- https://www.facebook.com/groups/505736576548648
- https://www.reddit.com/r/BIGTREETECH/
