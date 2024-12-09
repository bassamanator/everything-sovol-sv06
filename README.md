# Everything Sovol SV06

This branch contains `modifications` only.

Find specifications on the [main](https://github.com/bassamanator/everything-sovol-sv06) branch.

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
     - [CRTouch ✨](#crtouch)
     - [3DTouch ✨](#3dtouch)
     - [Beacon ✨](#beacon)
   - _Fans_
   - _Extruder_
2. [Motherboard](#motherboard)
3. [Lead Screws and Rods](#lead-screws-and-rods)
   - [Lead Screws](#lead-screws)
   - [Linear Motion Guide Rods](#linear-motion-guide-rods)
   - [Linear Bearings](#linear-bearings)
   - [Z Axis Couplers](#z-axis-couplers)
   - [Belts](#belts)
4. [PSU Related](#psu-related)
5. [Stepper Motors](#stepper-motors)

- [Support Me ❤️](#support-me)
- [Stay Up-to-Date](#stay-up-to-date)
- [Links](#useful-links)

# Hotend

## PCB

## Heatblock

### Heater Cartridge

### Thermistor

### Heatbreak

### Nozzle

## Filament Sensor

## Probe

### CRTouch

*This section is untested.*

*Reported by Reddit user Filahert.*

```
[bltouch]
sensor_pin:  ^PB1
control_pin:  PB0
x_offset: 30.0
y_offset: 0.0
speed: 20
stow_on_each_sample = false
samples: 1
```

### 3DTouch

![3D Touch](./images/probe/3dtouch.jpg)

### Beacon

⚠️ Everything found in this section is thanks to the user [1Euro7Cent](https://github.com/1Euro7Cent). I, [bassamanator](https://github.com/bassamanator), have not checked anything in this section, proceed with caution and common sense.

### Requirements

1. Klipper
   - running on a board that has an USB port. For example, a Raspberry Pi.
2. Aftermarket fan mod that puts the part cooling fan on the back of the extruder
3. [Beacon probe normal](https://beacon3d.com/product/beacon/) ~80$
4. [Beacon mount](./parts/beacon-mount-sovol-sv06-model_files)

### How-To

1. Print the [beacon mount](https://www.printables.com/model/459140-beacon-mount-sovol-sv06)
   - I recommend printing it in ABS or ASA because of the high temperature of the bed that could make the mount deform.
2. Set up Klipper (won't go into detail here)
3. Detach extruder plate from the extruder. (so that it is easier to work with)
   - Remove the ribbon cable from the extruder
   - Remove the 3 screws that hold the extruder plate to the extruder (that you can hold the whole extruder in your hand with the PCB still in place)
4. Remove the original probe
5. Attach the beacon probe to the beacon mount
   - use the screws that came with the beacon probe
   - the side where there is a hole at the top of the mount, don't screw the screw all the way in
6. Attach the USB cable to the beacon probe
7. Attach the beacon mount to the extruder motor (where the old probe was. Using the very same screw)
8. Fully but gently screw in the screw that you left loose in step 5. (it should go in the stepper motor case)
9. Re-attach the extruder plate to the extruder
   - Re-attach the 3 screws
   - Re-attach the ribbon cable
10. Route the USB cable to the board that is running Klipper, and plug it in.
11. secure the USB cable to the wire bundle with a few zip ties or something similar
12. follow the [quick start guide](https://docs.beacon3d.com/quickstart/)

### Broken down and simplified Klipper configs

printer.cfg

```yaml
[beacon]
serial: /dev/serial/by-path/<the assigned probe id>
# in other cases the id might be found in /dev/serial/by-id/usb-Beacon_Beacon_RevD_<the assigned probe id>-if00
x_offset: 0 # this is correct for the beacon mount that is linked above
y_offset: -17.42 # and this is correct too
mesh_main_direction: x
mesh_runs: 2
```

make sure that `[safe_z_home]` is in a save position

printer.cfg

```yaml
[safe_z_home]
home_xy_position: 85,135
z_hop: 5
z_hop_speed: 5
```

printer.cfg

```yaml
[stepper_z]
endstop_pin: probe:z_virtual_endstop # use beacon as virtual endstop
homing_retract_dist: 0 # beacon needs this to be set to 0
```

remove or comment out the existing `[probe]` section

make sure that you have a valid `[bed_mesh]` section
printer.cfg

```yaml
[bed_mesh]
speed: 100 # this is my fastest method without getting "spikes"
horizontal_move_z: 5
mesh_min: 20, 20
mesh_max: 210, 205
probe_count: 100,100 # change this to a number that is high enough but not too high. This works best for me
algorithm: bicubic
fade_start: 1
fade_end: 10
fade_target: 0
```

Save and restart klipper `systemctl restart klipper` or via the GUI.

### Calibrating the beacon probe

#### Home X and Y

```gcode
G28 X Y
```

#### Position probe in the center of the bed

```gcode
G1 X105 Y105
```

#### Move z to round about where the nozzle is close to the bed (not needed but makes it easier)

**WARNING**
This command can make the z axis crash into the bed. Adjust the distance accordingly. If you feel uncomfortable with this command, don't use it. If you use it, you are responsible for any damage that might occur.

The following command requires to have this in the printer.cfg set

```yaml
[force_move]
enable_force_move: True
```

This command force moves the z axis down 5mm at a speed of 5mm/s

```gcode
FORCE_MOVE STEPPER=stepper_z DISTANCE=-5 VELOCITY=5
```

if you are with in reason continue with the next step

#### Calibrate probe

```gcode
BEACON_CALIBRATE
```

#### Move z point closer for a paper test

```gcode
TESTZ Z=-0.01
```

#### Accept changes

```gcode
ACCEPT
```

#### Save config

```gcode
SAVE_CONFIG
```

#### Now you can home z

```gcode
G28 Z
```

#### And start a mesh

```gcode
BED_MESH_CALIBRATE
```

# Motherboard

# Lead Screws and Rods

## Lead Screws

## Linear Motion Guide Rods

## Linear Bearings

## Z Axis Couplers

## Belts

# PSU Related

# Stepper Motors

# Support Me

Please ⭐ star this repository!

If you found my work useful, consider buying me a [<img src="./images/misc/logo_white_stroke.png" height="20" alt='Ko-fi'/>](https://ko-fi.com/bassamanator).

# Stay Up-to-Date

This repository is a work in progress. Watch for updates:

<img src="./images/misc/githubstar.gif" width="500" alt='Github star'/>

# Useful Links

## Sovol Repositories

- [SV06 Official Marlin Source Code](https://github.com/Sovol3d/Sv06-Source-Code)
- [SV06 Official Models](https://github.com/Sovol3d/SV06-Fully-Open-Source)
- [SV06 Plus Official Marlin Source Code and Models](https://github.com/Sovol3d/SV06-PLUS)

## Useful Resources

- [_OSS_ Sovol SV06 Klipper Configuration](https://github.com/bassamanator/Sovol-SV06-firmware/tree/master)
- [RP2040-Zero ADXL345 Connection Klipper](https://github.com/bassamanator/rp2040-zero-adxl345-klipper)
- ⭐⭐⭐⭐⭐ [Ellis' Print Tuning Guide](https://ellis3dp.com/Print-Tuning-Guide)
- [Simplify3D Print Quality Troubleshooting Guide](https://www.simplify3d.com/resources/print-quality-troubleshooting/)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H0HIHTH)
