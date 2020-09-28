# Aquarius Mini Expander 1-1-0
Aquarius Mini Expander 1-1-0 - Rev B, 09 SEP 2020
 
by Sean P. Harrington, sph@1stage.com, http://aquarius.1stage.com
 
## Background
Since the Aquarius doesn't do much on it's own, and playing games on the chicklet keyboard is annoying, adding the functionality of the Mini Expander is essential. The Mini Expander expands the sounds to three voices, adds both a RAM and cartridge ROM expansion slot, and has ports for the Aquarius control pads. But since many Aquarius users DON'T have easy access to these devices, particularly in Europe, it was essential that this PCB be made available. 

## Purpose
The purpose of this project is to document the stock Aquarius Mini Expander, both in schematic form and in board layout. An excellent document from Radofin exists that records the original schematic for the device, and it was used to verify the components and layout of this project, but there are a few, minor discrepancies that have been corrected based on ACTUAL board layout. 

Also, this board serves as a useful prototype for how the expansion bus can be used on the Aquarius. By observing how the AY-3-8910 sound/IO chip is interfaced to the address and data bus, users who want to create their own expansion device could do so. Since it is already a very simple device (only about 25 components), the large footprint of the board could be improved through smaller SMD components and better trace routing, leaving plenty of room for additional functionality within the original (or modified) Mini Expander case.

## Bill of Materials
https://docs.google.com/spreadsheets/d/1Fgy7V73wTicvzhZblFc1MAg1R4uz7tYPBy140xyRtXA	

## Components
* Aquarius Mini Expander v1-1-0 PCB Rev B, 09 SEP 2020
* Electronic components (listed in BOM above)
* 3D printed parts
  * Aquarius Mini Expander v1-1-0 case BOTTOM
  * Aquarius Mini Expander v1-1-0 case TOP (in development)
  * Aquarius Mini Expander v1-1-0 case TRAP_FRONT (in development)
  * Aquarius Mini Expander v1-1-0 case TRAP_REAR (in development)
* Assembly screws (to be specified later)
* Trap Door springs (to be specified later)
* Trap Door hinges (to be specified later)

## Caveats
* This project does not incorpoate any new functionality. Users who want to add functionality may fork this project on their own.
  * SD Card read/write is not implemented, such as on the Micro Expander, a project developed by Bruce Abbott
  * A RAM expansion device is not included, such as the 32kb RAM Cartridge, a product developed by Jay Snellen, III
  * A cartridge ROM expansion device is not included, such as the AquariCart, a product developed by Jay Snellen, III
  * Switchable use of ATARI or SEGA joysticks (despite the same DB9 plugs)
* For users who want to use RAM or ROM in either cartridge slot, jumper pads (solder) have been added to connect pin 34 (rear slot) and/or pin 44 (front slot) to GND. Use this at your own discretion, but understand that you can't insert two ROM cartridges and expect them to work. Using two RAM cartridges could theoretically work, but it has not been tested.
* To maintain original layout, the three interconnect wires are not incorporated into the PCB. They are indicated as "WIRE" on the PCB, which should be bridged with 22 gauge solid core, insulated wire.
* The L1 choke/line filter (33uH) is difficult to source. Users may simply bridge this gap with 22 gauge solid core wire, or they can use a 0 ohm ferrite bead.
* Two of the small Control Pad interface boards are included as breakaways on either side of the narrow part of the board. These must be removed before the Mini Expander PCB can fit in the stock plastic shell. These small interface boards are used to transition the nine wires in the joystick cable to the mylar conductive pad used in the Control Pads.
