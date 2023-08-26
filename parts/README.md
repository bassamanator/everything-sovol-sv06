# Printed Parts

Please use common sense regarding material choice. If you're printing something that is touching the heated bed or near the hotend, use `PETG`/`ABS`/`other high temperature filament`.

## Essential

### Bed Cable Support

- Designer: [@rogerquin_304616](https://www.printables.com/@rogerquin_304616)
- Printer: SV06 / Plus
- [Source](https://www.printables.com/model/409689-heatbed-cable-support-for-sovol-sv06-3d-printer)
- [Download](SV06-heatbed-cable-support-V2.stl)

### Bed Cable Strain Relief

- Designer: [@rogerquin_304616](https://www.printables.com/@rogerquin_304616)
- Printer: SV06
- [Source](https://www.printables.com/model/409660-cable-strain-relief-for-sovol-sv06-3d-printer)
- If printing at <= 0.1mm layer height, [Download](./cable-strain-relief/SV06_heat_bed_cable_clamp_V1a.stl)
- If printing at >= 0.2mm layer height, [Download](./cable-strain-relief/SV06_heat_bed_cable_clamp_V1.stl)

## Useful

### Frame Mounting Solution

- Designer: [@bassamanator](https://www.printables.com/@bassamanator)
- Printer: SV06 / Plus
- Download from [here](https://www.printables.com/model/431736-sovol-sv06plus-frame-mounting-solution-2040-extrus).

### Part Cooling Fan Duct

- Designer: [taeky](https://cults3d.com/en/users/taeky/3d-models)
- Printer: SV06
- This is a paid model.
- There is a V2 of this model as well, but the performance according to the designer is the same. I prefer this version because it holds the duct more securely to the extruder assembly.
- [Sovol SV06 fan duct 5015 - CFD optimized](https://cults3d.com/:1021376)

### Extrusion Seals

- Designer: [@bassamanator](https://www.printables.com/@bassamanator)
- Printer: SV06 / Plus
- Download from [here](https://www.printables.com/model/385359-sovol-sv06plus-extrusion-seal).

# Initial Steps

Some of these steps might be seemingly unnecessary. For example, when I checked all the bolts on my SV06, all of them were perfectly tightened, but that might not always be the case with every unit. You have to decide what kind of experience you want to have with your printer. A printer that you have examined thoroughly is more reliable, and less likely to fail, than a printer that you have not put through these paces.

1. Check every bolt on the printer.
2. Check the filament gear grub screw. You can either check it periodically, or ideally, you should lock it in place with some low (or medium at most) strength threadlocker/loctite.
3. Lube the motion system. SavageLau has a good [video](https://youtu.be/lUvaA4fJWH0?) on this. The linear bearings on this printer as shielded, preventing dirt and other things such as a sufficient amount of lube, from getting inside. Packing the bearings with lube is _necessary_. I recommend [MOBILUX EP 2](https://www.grainger.ca/en/product/GREASE%2CMOBILUX-EP-2%2CGR390/p/ESO122132?analytics=orderHistory).
4. Adjust belt tension. This [video](https://user-images.githubusercontent.com/54855101/163674612-930d737d-0ab3-4056-a2b9-def2939db61f.mp4) is very helpful. You don't have to get very technical about this necessarily, just make sure the belts are firm, strummable like a guitar string. **Do not overtighten!**
5. Make sure the gantry is square. This [video](https://youtu.be/N5qbWdmn0VM) is useful.
6. If you are going to connect the printer to any kind of computer, you would be wise to use a USB cable that has the 5V pin 'disabled'. Read all about it [here](https://community.octoprint.org/t/put-tape-on-the-5v-pin-why-and-how/13574). I find that [thermal tape](https://s.click.aliexpress.com/e/_DEqaSAr) is easier to install than electrical tape. When everything is taped up correctly, your LCD screen will not light up when you connect it to a computer (PC, Raspberry Pi, etc.) _while the printer is off_.

<!-- $\small{\textcolor{darkturquoise}{\text{YOU ARE HERE}}}$ -->
