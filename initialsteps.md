# Initial Steps

_\* These steps should be followed for <u>any</u> budget printer_

Some of these steps might be seemingly unnecessary. For example, when I checked all the bolts on my SV06, all of them were perfectly tightened, but that might not always be the case with every unit. You have to decide what kind of experience you want to have with your printer. A printer that you have examined thoroughly is more reliable, and less likely to fail, than a printer that you have not put through these paces.

1. Check that every bolt on the printer is adequately tightened. ⚠️ _Do not overtighten!_
2. Apply some low strength (or medium _at most_) threadlocker/loctite to the [filament gear grub screw](./images/extruder-grub-screw.jpg). Alternatively, you can check this screw for tightness periodically (_not recommended_).
3. Lube the motion system. SavageLau has a good [video](https://youtu.be/lUvaA4fJWH0?) on this. The linear bearings on this printer as shielded, preventing dirt and other things such as a sufficient amount of lube, from getting inside. Packing the bearings with lube is _necessary_. I recommend [MOBILUX EP 2](https://www.grainger.ca/en/product/GREASE%2CMOBILUX-EP-2%2CGR390/p/ESO122132?analytics=orderHistory).
4. Adjust belt tension. This [video](https://user-images.githubusercontent.com/54855101/163674612-930d737d-0ab3-4056-a2b9-def2939db61f.mp4) is very helpful, you can read more about it [here](https://docs.vorondesign.com/tuning/secondary_printer_tuning.html#belt-tension). From that article, I prefer to the use `Carbon Drive` app, it's easy to use; aim for 110Hz. You don't necessarily have to get very technical about this, just make sure the belts are firm, strummable like a guitar string. ⚠️ _Do not overtighten!_
5. Make sure the gantry is square. This [video](https://youtu.be/N5qbWdmn0VM) is useful.
6. 1. Move the printhead and buildplate back and forth, through the _entire_ print range, by hand. Make sure there are no wires/cables that could obstruct the full, smooth range of motion.
   2. Now do the same again but using your printer's screen or dashboard (Mainsail, Fluidd, etc.).
7. [Retighten the nozzle](./howto.md#changing-nozzles), you will be sorry if you don't.
8. [Calibrate Esteps](./howto.md#calibrate-esteps).
9. If at any point you plan on connecting the printer to a computer, be sure to [put tape on the 5V pin](./howto.md#disable-usb-cable-5v-pin).

[Back](./README.md#outline)
