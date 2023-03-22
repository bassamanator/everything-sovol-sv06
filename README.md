# Everything Sovol SV06

A repository containing specifications of the Sovol SV06 3D printer parts, as well as links to aftermarket replacement parts.

Besides many hours, I have spent roughly ~~CAD$80~~ CAD$85 on unusable parts in order to find aftermarket replacements for the SV06. If you found this work useful, please consider buying me a [<img src="./misc/logo_white_stroke.png" height="20" alt='Ko-fi'/>](https://ko-fi.com/bassamanator).

You can also contribute by making a [pull-request](https://github.com/bassamanator/everything-sovol-sv06/pulls), creating an [issue](https://github.com/bassamanator/everything-sovol-sv06/issues), or starting a [discussion](https://github.com/bassamanator/everything-sovol-sv06/discussions).

*Some of the links found on this page may be affiliate links.*

## To do:

- [ ] Add stepper motor information.
- [x] Add Z coupler specs.
- [x] Add heatblock specs.
- [ ] Verify heatblock specs.
- [x] Add heatbreak specs.
- [ ] Add heater cartridge specs; no aftermarket source to be found.
- [ ] Add thermistor specs and aftermarket [source](https://s.click.aliexpress.com/e/_DmxAvaV).
- [X] Add PSU related information.

## Stay Up-to-Date

This repository is a work in progress. Watch for updates:

<img src="./images/githubstar.gif" width="500" alt='Github star'/>

## Hotend

### PCB SV06ZJB_V1.4

<img src="./images/hotend-pcb-labelled.png" width="800" alt='Hotend PCB'/>

| Label | Connection | PCB Connection | Other Connection | Other info |
| - | - | - | - | - |
| P3 | Coldend fan | JST 1.25mm 2-Pin |  |  |
| P2 | Extruder motor | JST 1.25mm 4-Pin | JST PH 2.0 6-Pin (*needs confirmation*) | Cable length 12cm |
| P4 | Heater cartridge | JST PH 2.0 2-Pin |  |  |
| P8 | Thermistor | JST 1.25mm 2-Pin |  |  |
| P6 | Probe  | JST 1.25mm 5-Pin |  |  |
| P5 | Part cooling fan | JST 1.25mm 2-Pin |  |  |
| P7 | Filament sensor | JST 1.25mm 3-Pin |  |  |

### Filament Sensor

I tested two random filament runout sensors that I had on hand. Both work just fine. It seems to me that any sensor with `VCC`, `Ground`, and `Signal` pins should work.

In order to get the filament sensor working, just make sure that the `VCC`, `Ground`, and `Signal` line up with the pins on the hotend PCB, port `P7`.

In order to 'mount' the sensor while it's not in use, simply glue a small magnet onto the sensor. You can then stick the sensor onto the extruder motor. You might also want to tether the sensor to the extruder cable with a piece of string.

Klipper filament configuration section:
```
[filament_switch_sensor filament_sensor]
switch_pin: !PA4 # "Pulled-high"
pause_on_runout: True
insert_gcode:
    M117 Insert Detected
runout_gcode:
    M117 Runout Detected
```

The complete Klipper code to make this work is part of my [OSS Klipper Configuration](https://github.com/bassamanator/Sovol-SV06-firmware).

<img src="./images/fil-sensor/btt.jpg" width="800" alt='Filament sensor'/>
<img src="./images/fil-sensor/simple.jpg" width="800" alt='Filament sensor'/>
<img src="./images/fil-sensor/fil-sensor-side.jpg" width="800" alt='Filament sensor'/>

#### Aftermarket Options

These can be found for very cheap (roughly $1.5) on Aliexpress and quite a bit more on  Amazon (though still very afforable). [This](https://s.click.aliexpress.com/e/_DDLpdBX) is the one I bought. Here's another seemingly [viable option](https://s.click.aliexpress.com/e/_DDPNmDX).

##### How To Cable

You need to make your own cable. I recommend getting these [JST 1.25 cables](https://s.click.aliexpress.com/e/_DDORZ0D), and this [XH2.54 kit](https://s.click.aliexpress.com/e/_DlejPpj). You will also need a crimping tool such as the [Engineer PA-09](https://www.amazon.ca/gp/product/B002AVVO7K/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1).
### Heatblock

The heatblock the SV06 uses is a Creality CR10 heatblock with support for an M6 threaded nozzle (including some MK8 nozzles). It has support for a [cartridge heater](https://www.aliexpress.com/item/32817471679.html?spm=a2g0o.productlist.main.21.398f5950SZin7w&algo_pvid=a02d1fa0-6027-439b-80b9-3dfd6d9066bf&algo_exp_id=a02d1fa0-6027-439b-80b9-3dfd6d9066bf-10&pdp_ext_f=%7B%22sku_id%22%3A%2265398686104%22%7D&pdp_npi=3%40dis%21CAD%211.49%211.18%21%21%21%21%21%40211bf3f116794791211837332d0761%2165398686104%21sea%21CA%214666093930&curPageLogUid=QZs3XELKua4B) (6mm) and a [glass-bead thermistor](https://www.aliexpress.com/item/32514751406.html?spm=a2g0o.productlist.main.13.4fc51vs51vs5FC&algo_pvid=4a9f6fcc-9db5-4db7-91e2-68112b03071e&aem_p4p_detail=202303220250351111396485568820005062336&algo_exp_id=4a9f6fcc-9db5-4db7-91e2-68112b03071e-6&pdp_ext_f=%7B%22sku_id%22%3A%2265732281353%22%7D&pdp_npi=3%40dis%21CAD%211.63%211.54%21%21%21%21%21%402102176616794786350847201d0767%2165732281353%21sea%21CA%214666093930&curPageLogUid=ShRbt8qZkw2q&ad_pvid=202303220250351111396485568820005062336_7&ad_pvid=202303220250351111396485568820005062336_7) (2mm). The heatblocks on AliExpress normally come in Brass, Copper Plated and Aluminum. Copper plated offers the best thermal conductivity of all of them which makes it the better option.


<p align="center">
<img src="./images/heatblock/heatblock-display.jpg" height="130" alt='Heatblock image'/>

| Height | Length | Thickness |
| - | - | - |
| 20mm | 20mm| 10mm|

<img src="./images/heatblock/heatblock-specs.png" width="500" alt='Heatblock spec'/>

</p>

#### Heater Cartridge
The SV06 uses a ceramic heater cartridge which is 40W 12v *(needs looking into)*. It has a [JST-PH 2-pin connector](https://www.aliexpress.com/item/32908472053.html?spm=a2g0o.productlist.main.27.34a07842VA0u0U&algo_pvid=56fd3a56-ea45-49a0-97aa-151e49fb898e&algo_exp_id=56fd3a56-ea45-49a0-97aa-151e49fb898e-13&pdp_ext_f=%7B%22sku_id%22%3A%2265895534505%22%7D&pdp_npi=3%40dis%21CAD%212.89%212.89%21%21%21%21%21%40211bea6216794812702558054d06fe%2165895534505%21sea%21CA%214666093930&curPageLogUid=KEzsCq1b9bZr) to be used with the SV06 PCB. The heater cartridge usually has some thermal paste on it to help with heat transfer, any thermal paste will work.


#### Thermistor Glass-Bead
Most CR10 heatblocks use a [glass-bead thermistor](https://en.wikipedia.org/wiki/Thermistor) with the resistence of the thermistor getting higher as the tempeture increases. The thermistor size that is supported with the stock heatblock is 2mm in diameter which is what the glass bead thermistor uses. The stock thermistor has a [JST 1.25mm 2-pin](https://www.aliexpress.com/item/1005004931013896.html?spm=a2g0o.cart.0.0.6fac38da0aHMsB&mp=1) connector to connect to the PCB.

<details>
<summary>Cartridge Thermistor DIY</summary>
<br>
Some people prefer the Thermistor Cartridge type thermistor because of it's higher durability, ease to use and a larger variety. But I have not found any CR10 heatblocks which support it, meaning the DIY method for supporting the cartridge thermistor would be to drill it with a 1/8 (3mm) drill bit.
</details>
<br>

#### Aftermarket Options
Aftermarket options include various items from [AliExpress](aliexpress.com) and [Ebay](ebay.com).

[//]: <> (//todo Needs links to Aliexpress and Ebay sites)

### Heatbreak

<img src="./images/heatbreak/heatbreak.png" height="200" alt=''/>

| Cooper Portion | Overall Length | Outer Dia. | Inner Dia. |
| - | - | - | - |
| 15mm | 22mm | 7mm| 2mm|

<img src="./images/heatbreak/copper-portion.jpg" width="100" alt='Heatbreak spec'/>
<img src="./images/heatbreak/overall.jpg" width="100" alt='22mm'/>
<img src="./images/heatbreak/od.jpg" width="100" alt='Heatbreak spec'/>

#### Aftermarket Options

I purchased and tested [this heatbreak](https://s.click.aliexpress.com/e/_DmzWJNb). It works as well as the stock piece.

*The part sold in the link could change, so make sure it has the following specs*:

<img src="./images/heatbreak/aftermarket-aliexpress.png" height="200" alt='Aftermarket heatbreak'/>

## Motherboard

<img src="./images/motherboard.png" width="800" alt='Motherboard'/>

## Lead Screws and Rods

### Lead Screws

| Axis | Qty | Length | Dia. | Lead | Pitch | Starts | Sovol Part # |
| - | - | - | - | - | - | - | - |
| Z | 2 | 376mm | 8mm | 4mm | 2mm | 2 | JXHSV06-02003-a |

### Linear Motion Guide Rods

| Axis | Qty | Length | Dia. | Sovol Part # |
| - | - | - | - | - |
| X | 2 | 350mm | 8mm | JXHSV06-03001-a |
| Y | 2 | 340mm | 8mm | JXHSV06-01012-a |
| Z | 2 | 400mm | 8mm | JXHSV06-02004-a |

## Z Axis Couplers

<img src="./images/z-coupler.png" width="100" alt='Z coupler rigid 5mm to 8mm'/>

| Type | Qty | Dia.| Length | Motor Shaft Dia. | Lead Screw Dia. |
| - | - | - | - | - | - |
| Rigid | 2 | 20mm | 25mm | 5mm | 8mm |

## PSU Related

<img src="./images/psu/psu-label.jpg" width='400px' alt=''/>

### PSU Connections

<img src="./images/psu/PSU-line-connections.png" alt=''/>

### PSU Switch

<img src="./images/psu/switch.png" alt=''/>
<img src="./images/psu/switch-wiring.png" alt=''/>
<img src="./images/psu/switch-wiring-alt.png" alt=''/>

### Other PSU Cable

<img src="./images/psu/XT60H-M-1.jpg" width='200' alt=''/>
<img src="./images/psu/XT60H-M-2.jpg" width='200' alt=''/>
<img src="./images/psu/XT60H-M-3-edit.jpg" width='400' alt=''/>

## Sovol Repositories

- [Marlin source code](https://github.com/Sovol3d/Sv06-Source-Code)
- [Printer parts STL and STEP files](https://github.com/Sovol3d/SV06-Fully-Open-Source)

## Useful Resources

- [*OSS* Sovol SV06 Klipper Configuration](https://github.com/bassamanator/Sovol-SV06-firmware/tree/master)
- [RP2040-Zero ADXL345 Connection Klipper](https://github.com/bassamanator/rp2040-zero-adxl345-klipper)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H0HIHTH)
