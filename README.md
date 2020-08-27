# Aquarius Mini Expander 1-1-0
Aquarius Mini Expander 1-1-0 - Rev A
 
by Sean P. Harrington, sph@1stage.com, http://aquarius.1stage.com
 
## Background
Since the Aquarius doesn't do much on it's own, and playing games on the chicklet keyboard is annoying, adding the functionality of the Mini Expander is essential. The Mini Expander expands the sounds to three voices, adds both a RAM and cartridge expansion slot, and has ports for the Aquarius control pads. But since many Aquarius users DON'T have easy access to these devices, particularly in Europe, I felt it was essential that this PCB be made available. 

## Purpose
The purpose of this project is to document the stock Aquarius Mini Expander, both in schematic form and in board layout. An excellent document from Radofin exists that records the original schematic for the device, and it was used to verify the components and layout of this project, but there are a few, minor discrepancies that have been corrected based on ACTUAL board layout. Similarly, layout issues on the board have been corrected based on the documentation (i.e. GND pins 24 and 44 of the front and back expansion slots are not consistently wired to the GND plane.)

Also, this board serves as an excellent prototype for how the expansion bus can be used on the Aquarius. By observing how the AY-3-8910 sound/IO chip is interfaced to the address and data bus, users who want to create their own expansion device could do so. Since it is already a very simple device (only about 25 components), the large footprint of the board could be improved through smaller SMD components and better trace routing, leaving plenty of room for additional functionality within the original (or modified) Mini Expander case.
