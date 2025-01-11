# Everything Sovol SV06

A repository containing specifications of the Sovol SV06 3D printer parts, as well as links to aftermarket replacement parts.

You can assume that all information herein is accurate unless stated otherwise.

If you found this work useful, please consider buying me a [<img src="./images/misc/logo_white_stroke.png" height="20" alt='Ko-fi'/>](https://ko-fi.com/bassamanator).

You can also contribute by making a [pull-request](https://github.com/bassamanator/everything-sovol-sv06/pulls), creating an [issue](https://github.com/bassamanator/everything-sovol-sv06/issues), or starting a [discussion](https://github.com/bassamanator/everything-sovol-sv06/discussions).

_Some of the links found on this page may be affiliate links._

# Outline

1. [Hotend](#hotend)
   - [PCB](#pcb)
   - [Heatblock](#heatblock)
     - [Heater Cartridge](#heater-cartridge)
     - [Thermistor](#thermistor)
     - [Heatbreak](#heatbreak)
     - [Nozzle](#nozzle)
   - [Filament Sensor](#filament-sensor)
   - [Probe](#probe)
   - _Fans_
   - [Extruder](#extruder)
2. [Motherboard](#motherboard)
3. [Lead Screws and Rods](#lead-screws-and-rods)
   - [Lead Screws](#lead-screws)
   - [POM Nuts](#pom-nuts)
   - [Linear Motion Guide Rods](#linear-motion-guide-rods)
   - [Linear Bearings](#linear-bearings)
   - [Z Axis Couplers](#z-axis-couplers)
   - [Belts](#belts)
4. [PSU Related](#psu-related)
5. [Stepper Motors](#stepper-motors)

- [Initial Steps ⚡](./initialsteps.md)
- [Printed Upgrades 🏗️](./parts/README.md#printed-parts)
- [Sample Prints 🍰](./images/prints/README.md)
- [How-to 🛠️](./howto.md)
- [Modifications 🪚](https://github.com/bassamanator/everything-sovol-sv06/tree/mods)
- [Support Me ❤️](#support-me)
- [Stay Up-to-Date](#stay-up-to-date)
- [Links](#links)

# Hotend

## PCB

Revision: `SV06ZJB_V1.4`

<img src="./images/hotend-pcb-labelled.png" width="800" alt='Hotend PCB'/>

| Label | Connection       | PCB Connection        | Other Connection | Other info        |
| ----- | ---------------- | --------------------- | ---------------- | ----------------- |
| P3    | Coldend fan      | Molex PicoBlade 2-Pin |                  |                   |
| P2    | Extruder motor   | Molex PicoBlade 4-Pin | JST PH 2.0 6-Pin | Cable length 12cm |
| P4    | Heater cartridge | JST PH 2.0 2-Pin      |                  |                   |
| P8    | Thermistor       | Molex PicoBlade 2-Pin |                  |                   |
| P6    | Probe            | Molex PicoBlade 5-Pin |                  |                   |
| P5    | Part cooling fan | Molex PicoBlade 2-Pin |                  |                   |
| P7    | Filament sensor  | Molex PicoBlade 3-Pin |                  |                   |

\* _Note, Molex PicoBlade are often mischaracterized as JST 1.25mm (the name under which they are usually sold online)._

## Heatblock

<img src="./images/heatblock/heatblock-display.jpg" height="100" alt='Heatblock image'/>

| Model         | Material |
| ------------- | -------- |
| Creality CR10 | Aluminum |

Notes:

- The heatblock is mounted onto the extruder assembly using `2 x M2.5 x 10mm` [SHCS](./images/shcs.png).
- Newer heatblocks appear to have a 3mm thermistor hole.

<p align="center">
<img src="./images/heatblock/heatblock-specs.png" width="500" alt='Heatblock spec'/>
</p>

### Aftermarket Options

Any of [these](https://s.click.aliexpress.com/e/_Dle8W0N) heatblocks will do just fine, however, they _may_ require mounting bolts of different sizes.

- The [Type C](https://s.click.aliexpress.com/e/_DEfTKT1) has 2mm and 3mm thermistor holes.
- I have the `Type C`. The original mounting bolts will not be long enough, you will need [2 x M2.5 x 16mm FHCS](https://s.click.aliexpress.com/e/_DFDH4Hl) ([2 x M2.5 x 18mm FHCS](https://s.click.aliexpress.com/e/_DEbXHQ7) will also work).

### Heater Cartridge

The SV06 uses a ceramic heater cartridge.

| Voltage | Watts | Dimensions | Connection       | Cable Length |
| ------- | ----- | ---------- | ---------------- | ------------ |
| 24V     | 50W   | 6x20mm     | JST PH 2.0 2-Pin | ~40mm        |

The heater cartridge is glued into the heatblock, a heatblock that heats to 300C. Although possible, it is inadvisable, and potentially dangerous to attempt removal.

#### Aftermarket Options

Unfortunately, a direct, non-DIY replacement seems unlikely. It appears that no one sells heater cartridges with JST PH 2.0 2-Pin connectors.

You would have to buy a heater cartridge such as [this](https://s.click.aliexpress.com/e/_DeKbxqv), and crimp the appropriate connector on.

⚠️ This is not an ordinary crimp job. The hotend assembly consumes a lot of power and is dangerously hot. Take every precaution.

### Thermistor

| Material   | Dimensions | Connection            | Cable Length |
| ---------- | ---------- | --------------------- | ------------ |
| Glass-bead | 2mm        | Molex PicoBlade 2-Pin | ~40mm        |

The thermistor is held in place with the help of a screw, and a generous amount of thermal adhesive. With the help of a heat-gun, and with great care, it can be removed.

#### Aftermarket Options

- [3mm Tube Thermistor](https://s.click.aliexpress.com/e/_DnBUliL)
  - Please note that this thermistor will **not** fit in the stock heatblock. You need a heatblock that has a 3mm thermistor hole.
- [3mm Tube Thermistor 4 units](https://s.click.aliexpress.com/e/_Dmwf20F)
  - **Untested** though it looks exactly the same as the option above.
  - Cheaper than then first option.
  - Please note that this thermistor will **not** fit in the stock heatblock. You need a heatblock that has a 3mm thermistor hole.

### Heatbreak

<!-- <img src="./images/heatbreak/heatbreak.png" height="200" alt=''/> -->

<img src="./images/heatbreak/heatbreak-original.jpg" height="200" alt='Heatbreak original'/>

| Cooper Portion | Overall Length | Outer Dia. | Inner Dia. |
| -------------- | -------------- | ---------- | ---------- |
| 15mm           | 22mm           | 7mm        | 2mm        |

#### Aftermarket Options

I purchased and tested [this heatbreak](https://s.click.aliexpress.com/e/_DmzWJNb).

- It works as well as the stock piece.
- ⚠️ It is 1mm shorter than the stock piece, so you will need a washer or spacer of some kind to 'increase' it's length. If you don't add a spacer, your part cooling duct will be exactly inline with the nozzle tip, meaning that the part cooling duct will drag across every new layer. The spacer must not be more than 7mm in diameter.

_The part sold in the link could change, so make sure it has the following specs_:

<img src="./images/heatbreak/aftermarket-aliexpress.png" height="200" alt='Aftermarket heatbreak'/>

### Nozzle

<img src="./images/nozzle/mk8-nozzle.jpg" height="200" alt=''/>

| Type | Thread |
| ---- | ------ |
| MK8  | M6     |

Any MK8 nozzle will do. You can even use a [V6 style nozzle](./images/nozzle/nozzle-comparison.jpg).

#### Aftermarket Options

**Any** MK8 nozzle will be fine. I like [these](https://s.click.aliexpress.com/e/_DCDKb0n) because they're chunky.

##### SV06 Plus

A Creality K1 nozzle seems like a suitable replacement (_needs verification_), however, it is 0.5mm shorter than the stock variant. You have to make use of a washer/spacer to correct for this, see [Heatbreak, Aftermarket](#aftermarket-options-3) section.

## Filament Sensor

I tested two random filament runout sensors that I had on hand. Both work just fine. It seems to me that any sensor with `VCC`, `Ground`, and `Signal` pins should work.

In order to get the filament sensor working, just make sure that the `VCC`, `Ground`, and `Signal` line up with the pins on the hotend PCB, port `P7`.

<details>
<summary>Alternate connection</summary>
You can connect the sensor directly to the motherboard's `Pre-set port`. By default, this port has the `DET` cable connected to it.
</details>

In order to 'mount' the sensor while it's not in use, simply glue a small magnet onto the sensor. You can then stick the sensor onto the extruder motor. You might also want to tether the sensor to the extruder cable with a piece of string.

### Klipper configuration

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

### Aftermarket Options

These can be found for very cheap (roughly $1.5) on Aliexpress and quite a bit more on Amazon (though still very affordable). [This](https://s.click.aliexpress.com/e/_DDLpdBX) is the one I bought. Here's another seemingly [viable option](https://s.click.aliexpress.com/e/_DDPNmDX).

### Cable How-To

You need to make your own cable. I recommend getting these [JST 1.25 cables](https://s.click.aliexpress.com/e/_DDORZ0D), and this [XH2.54 kit](https://s.click.aliexpress.com/e/_DlejPpj). You will also need a crimping tool such as the [Engineer PA-09](https://www.amazon.ca/gp/product/B002AVVO7K/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1).

## Probe

<p align="center">
    <img src="./images/probe/probe.png" height="600" alt='probe'/>
</p>
<p align="center">
<img src="./images/probe/pinoutribboncable.png" height="400" alt='probe'/>
</p>

| Part          | Voltage | Type                  | Measuring Distance |
| ------------- | ------- | --------------------- | ------------------ |
| LJ12A3-4-Z-AX | ~5V      | NPN (normally closed) | ~4mm               |

### Aftermarket Options

- I bought this probe [LJ12A3-4-ZAX](https://s.click.aliexpress.com/e/_olGmrWv). _Completely untested_.
- Another option [LJ12A3-4-Z-AX](https://s.click.aliexpress.com/e/_Dm2TIhh). _Completely Untested_.

## Extruder

The parts from a DIY Orbiter V1.5 kit are suitable replacements for this extruder. I'll do a more thorough write-up eventually, but in the meantime, the only parts that differ in the Orbiter are:

- the 3 pronged stem is longer in the Orbiter though that should not be an issue.
- the flanged bearing has a larger OD in the Orbiter.
- I did not compare the filament gears.

After over 600 hours of print time, I saw hardly any wear on the gears in the extruder.

### Aftermarket Options

- [This](https://s.click.aliexpress.com/e/_DE2NRWZ) is the Orbiter kit that I bought and took measurements from, but any other V1.5 kit should do fine.
- [Mellow](https://s.click.aliexpress.com/e/_DdpgYhT) has a great option as well.

# Motherboard

<p align="center">
    <img src="./images/motherboard.png" width="400" alt='Motherboard' />
</p>

### Aftermarket Options

I haven't seen this particular board around, though it should be easy enough to purchase from Sovol3d directly. Having said that, the `SKR-Mini-E3-V2.0/V3.0` are viable replacements that fit perfectly in the stock motherboard enclosure, and likely cheaper than the original board. I would recommend the `V3.0` over the `V2.0 `because I have a hardware guide and a Klipper configuration ready to go on my OSS repository, find link below.

# Lead Screws and Rods

## Lead Screws

<img src="./images/lead-screw.png " width="300" alt='Lead screw' />

| Axis | Qty | Length | Dia. | Lead | Pitch | Starts | Sovol Part #    |
| ---- | --- | ------ | ---- | ---- | ----- | ------ | --------------- |
| Z    | 2   | 376mm  | 8mm  | 4mm  | 2mm   | 2      | JXHSV06-02003-a |

## POM Nuts

| Material                           | Dia. | Lead | Pitch |
| ---------------------------------- | ---- | ---- | ----- |
| Polyoxymethylene (type of plastic) | 8mm  | 4mm  | 2mm   |

### Aftermarket Options

I have been unable to find _direct_ replacements. I am using [these](https://s.click.aliexpress.com/e/_DBMjmq3), however, you will likely have to drill out the attachment holes with a 3mm drill bit (very easy and quick modification). Please note that I'm not using them as anti-backlash nuts, so that portion of these parts will likely go unused.

## Lead Rods

<img src="./images/lead-rod.webp " width="300" alt='Lead rod' />

| Axis | Qty | Length | Dia. | Sovol Part #    |
| ---- | --- | ------ | ---- | --------------- |
| X    | 2   | 355mm  | 8mm  | JXHSV06-03001-a |
| Y    | 2   | 340mm  | 8mm  | JXHSV06-01012-a |
| Z    | 2   | 400mm  | 8mm  | JXHSV06-02004-a |

## Linear Bearings

<img src="./images/linear-bearings2.webp" width="200" alt='Motherboard' />

| Type           | Part  | Quantity |
| -------------- | ----- | -------- |
| Linear bearing | LM8UU | 10       |

## Z Axis Couplers

<img src="./images/z-coupler.png" width="100" alt='Z coupler rigid 5mm to 8mm'/>

| Type  | Qty | Dia. | Length | Motor Shaft Dia. | Lead Screw Dia. |
| ----- | --- | ---- | ------ | ---------------- | --------------- |
| Rigid | 2   | 20mm | 25mm   | 5mm              | 8mm             |

### Aftermarket Options

[Option 1](https://s.click.aliexpress.com/e/_DFQu2bD)

## Belts

<img src="./images/belt.png" width="300" alt='belt 6mm'/>

| Brand | Part                 | Length | Width |
| ----- | -------------------- | ------ | ----- |
| GATES | PowerGrip GT2 LL-2GT | ~1.5m  | 6mm   |

### Aftermarket Options

Two meters will handle both the Y and X axis.

- [GATES](https://s.click.aliexpress.com/e/_DCMqSrf)
- [POWGE](https://s.click.aliexpress.com/e/_Dei89Ul)
  - I use these myself, they're top quality.

### Timing Belt Toothed Pulleys

_Coming soon._

### Timing Belt Smooth Idlers

![Smooth Idlers](./images/smooth-idler.jpg)

# PSU Related

| Brand       | Model    | Wattage | Voltage |
| ----------- | -------- | ------- | ------- |
| Cheng Liang | P360W24V | 360W    | 24V     |

<img src="./images/psu/psu-label.jpg" width='400px' alt=''/>

## PSU Connections

<img src="./images/psu/PSU-line-connections.jpg" alt=''/>

## PSU Switch

<img src="./images/psu/switch.jpg" alt=''/>
<img src="./images/psu/switch-wiring.jpg" alt=''/>
<img src="./images/psu/switch-wiring-alt.jpg" alt=''/>

## Other PSU Cable

| Part      |
| --------- |
| XT60H-M/F |

![PSU cable](./images/psu/xt60h-m-3-combined.jpg)

## Internal Fan Cable Connector

<img src="./images/psu/psu-fan-connector.jpg" width="300" alt='PSU fan connector'/>

| Printer   | Part   | Pitch  |
| --------- | ------ | ------ |
| SV06      | JST-XA | 2.54mm |
| SV06 Plus | JST-XH | 2.54mm |

# Stepper Motors

<img src="./images/stepper-motor.webp" width="300" alt='Stepper motor'/>

| Location   | Motor   | Height | Peak current                | Step angle |
| ---------- | ------- | ------ | --------------------------- | ---------- |
| Extruder   | Nema 17 | 22     | 0.8A (_needs verification_) | 1.8°       |
| X-Gantry   | Nema 17 | 34     | 1.3A                        | 1.8°       |
| Y-Axis     | Nema 17 | 34     | 1.3A                        | 1.8°       |
| 2 x Z-Axis | Nema 17 | 34     | 1.3A                        | 1.8°       |

## Y-Axis

- In case you need to replace it, you can _probably_ fit a stepper motor with a height of 42mm.
- A stepper motor with a height of 40mm will certainly fit.

## Aftermarket Options

### Notes:

- Adjusting the connectors will likely be required for any replacement stepper.
- If using Klipper, it will be very easy to adapt the `printer.cfg` for these steppers.
- If using Marlin, you will either have to compile your own firmware, or it might be possible to adjust the current via the menu.
- The links for aftermarket options have good specifications, however, they are _completely untested_.

### Options

- [X-Gantry and Z-Axis](https://s.click.aliexpress.com/e/_DeYggkp)
  - I would go for the 42mm height steppers myself.
- [Y-Axis](https://s.click.aliexpress.com/e/_DelgWct)

# Support Me

Please ⭐ star this repository!

Support [open source](https://en.wikipedia.org/wiki/Open_source), and buy me a [<img src="./images/misc/logo_white_stroke.png" height="20" alt='Ko-fi'/>](https://ko-fi.com/bassamanator).

# Stay Up-to-Date

This repository is a work in progress. Watch for updates:

<img src="./images/misc/githubstar.gif" width="500" alt='Github star'/>

# Links

## Useful Resources

- [_OSS_ Sovol SV06 Klipper Configuration](https://github.com/bassamanator/Sovol-SV06-firmware/tree/master)
- [RP2040-Zero ADXL345 Connection Klipper](https://github.com/bassamanator/rp2040-zero-adxl345-klipper)
- ⭐⭐⭐⭐⭐ [Ellis' Print Tuning Guide](https://ellis3dp.com/Print-Tuning-Guide)
- [Simplify3D Print Quality Troubleshooting Guide](https://www.simplify3d.com/resources/print-quality-troubleshooting/)

## Sovol Official Links

- [SV06 Marlin Source Code](https://github.com/Sovol3d/Sv06-Source-Code)
- [SV06 Models](https://github.com/Sovol3d/SV06-Fully-Open-Source)
- [SV06 Plus Marlin Source Code and Models](https://github.com/Sovol3d/SV06-PLUS)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H0HIHTH)
