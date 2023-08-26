# Initial Steps

Some of these steps might be seemingly unnecessary. For example, when I checked all the bolts on my SV06, all of them were perfectly tightened, but that might not always be the case with every unit. You have to decide what kind of experience you want to have with your printer. A printer that you have examined thoroughly is more reliable, and less likely to fail, than a printer that you have not put through these paces.

1. Check every bolt on the printer.
2. Check the filament gear grub screw. You can either check it periodically, or ideally, you should lock it in place with some low strength (or medium _at most_) threadlocker/loctite.
3. Lube the motion system. SavageLau has a good [video](https://youtu.be/lUvaA4fJWH0?) on this. The linear bearings on this printer as shielded, preventing dirt and other things such as a sufficient amount of lube, from getting inside. Packing the bearings with lube is _necessary_. I recommend [MOBILUX EP 2](https://www.grainger.ca/en/product/GREASE%2CMOBILUX-EP-2%2CGR390/p/ESO122132?analytics=orderHistory).
4. Adjust belt tension. This [video](https://user-images.githubusercontent.com/54855101/163674612-930d737d-0ab3-4056-a2b9-def2939db61f.mp4) is very helpful. Read more about it [here](https://docs.vorondesign.com/tuning/secondary_printer_tuning.html#belt-tension), but you don't necessarily have to get very technical about this. Just make sure the belts are firm, strummable like a guitar string. **Do not overtighten!**
5. Make sure the gantry is square. This [video](https://youtu.be/N5qbWdmn0VM) is useful.
6. [Put tape on the 5V pin](./README.md#put-tape-on-the-5v-pin).

## Put tape on the 5V pin

If you are going to connect the printer to any kind of computer (PC, laptop, Raspberry Pi, etc.), you would be wise to use a USB cable that has the 5V pin 'disabled'. Read all about it [here](https://community.octoprint.org/t/put-tape-on-the-5v-pin-why-and-how/13574). I find that [thermal tape](https://s.click.aliexpress.com/e/_DEqaSAr) is easier to install than electrical tape. When everything is taped up correctly, the LCD screen will not light up when a powered off printer is connected to a computer.
