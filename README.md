# Everything Sovol SV06

A repository containing specifications of the Sovol SV06 3D printer parts.

Please contribute by making a [pull-request](https://github.com/bassamanator/everything-sovol-sv06/pulls), creating an [issue](https://github.com/bassamanator/everything-sovol-sv06/issues), or starting a [discussion](https://github.com/bassamanator/everything-sovol-sv06/discussions).

To do:

- [ ] Add stepper motor information.

## Hotend

### SV06ZJB_V1.4

<img src="./images/hotend-pcb-labelled.png" width="800" alt='Raspberry Pi'/>

| Label | Connection | PCB Connection | Other Connection | Other info |
| ------------ | ----------- | ------------ | ----------- | ----------- |
| P3           | Coldend fan      | JST 1.25mm 2-Pin |  |  |
| P2           | Extruder motor   | JST 1.25mm 4-Pin | JST PH 2.0 6-Pin \**needs confirmation* | Cable length 12cm |
| P4           | Heater cartridge | JST PH 2.0 2-Pin |  |  |
| P8           | Thermistor       | JST 1.25mm 2-Pin |  |  |
| P6           | Probe            | JST 1.25mm 5-Pin |  |  |
| P5           | Part cooling fan | JST 1.25mm 2-Pin |  |  |
| P7           | ??Filament sensor??| JST 1.25mm 3-Pin |  |  |

## Motherboard

<img src="./images/motherboard.png" width="800" alt='Raspberry Pi'/>

## Lead Screws and Rods

<img src="./images/Lead_screws_specs.PNG" width="800" alt='Raspberry Pi'/>

<img src="./images/Rods_specs.PNG" width="800" alt='Raspberry Pi'/>

## Sovol Repositories

- [Marlin source code](https://github.com/Sovol3d/Sv06-Source-Code)
- [Printer parts STL and STEP files](https://github.com/Sovol3d/SV06-Fully-Open-Source)

## Useful Resources

- [*OSS* Sovol SV06 Klipper Configuration](https://github.com/bassamanator/Sovol-SV06-firmware/tree/master)
- [RP2040-Zero ADXL345 Connection Klipper](https://github.com/bassamanator/rp2040-zero-adxl345-klipper)