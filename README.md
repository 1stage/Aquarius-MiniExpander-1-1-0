# Aquarius Mini Expander 1-1-0
Aquarius Mini Expander 1-1-0 - Rev A
 
by Sean P. Harrington, sph@1stage.com, http://aquarius.1stage.com
 
## Background
Since the Aquarius doesn't do much on it's own, and playing games on the chicklet keyboard is annoying, adding the functionality of the Mini Expander is essential. The Mini Expander expands the sounds to three voices, adds both a RAM and cartridge expansion slot, and has ports for the Aquarius control pads. But since many Aquarius users DON'T have easy access to these devices, particularly in Europe, it was essential that this PCB be made available. 

## Purpose
The purpose of this project is to document the stock Aquarius Mini Expander, both in schematic form and in board layout. An excellent document from Radofin exists that records the original schematic for the device, and it was used to verify the components and layout of this project, but there are a few, minor discrepancies that have been corrected based on ACTUAL board layout. 

Also, this board serves as an excellent prototype for how the expansion bus can be used on the Aquarius. By observing how the AY-3-8910 sound/IO chip is interfaced to the address and data bus, users who want to create their own expansion device could do so. Since it is already a very simple device (only about 25 components), the large footprint of the board could be improved through smaller SMD components and better trace routing, leaving plenty of room for additional functionality within the original (or modified) Mini Expander case.

## Bill of Materials
* C1	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725983	
* C2	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725984	
* C3	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725985	
* C4	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725986	
* C5	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725987	
* C6	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725988	
* C7	Capacitor, Ceramic, 6.4mm pitch, outline 2.5 x 9mm	100nF	https://www.digikey.com/product-detail/en/kemet/C321C104M5U5TA/399-9786-ND/3725989	
* C8	Capacitor, Electrolytic Polarized, Axial through hole, 22mm pitch, 6mm diameter	10uF @ 16v	https://www.digikey.com/product-detail/en/106TTA035M/1572-1653-ND/5410705	
* C9	Capacitor, Ceramic, 3.2mm pitch, outline 1 x 3.2mm	10nF @ 50v	https://www.digikey.com/product-detail/en/kemet/C410C103K5R5TA7200/399-4452-1-ND/818309	
* C10	Capacitor, Ceramic, 3.2mm pitch, outline 1 x 3.2mm	10nF @ 50v	https://www.digikey.com/product-detail/en/kemet/C410C103K5R5TA7200/399-4452-1-ND/818309	
* J1	Edge Connector, Female, 2x22 pins, 2.54pitch, straight	TE AMP 5530843-4	https://www.digikey.com/product-detail/en/te-connectivity-amp-connectors/5530843-4/A31717-ND/770543	
* J2	Edge Connector, Female, 2x22 pins, 2.54pitch, straight	TE AMP 5530843-4	https://www.digikey.com/product-detail/en/te-connectivity-amp-connectors/5530843-4/A31717-ND/770543	
* J3	DB9, boardlock, Male, Right angle	TE 5745001-3	https://www.digikey.com/product-detail/en/te-connectivity-amp/5745001-3/A34003-ND/	
* J4	DB9, boardlock, Male, Right angle	TE 5745001-3	https://www.digikey.com/product-detail/en/te-connectivity-amp/5745001-3/A34003-ND/	
* L1	Radial formal inductor, outline 2.04 x 5mm	33uH	(ok to replace with wire)	
* Q1	Transistor 2N3904 NPN, TO-92 CBE	40V, 0.2A	https://www.digikey.com/product-detail/en/on-semiconductor/2N3904BU/2N3904FS-ND/1413	
* R1	Resistor, 1/4W 0207/7	10k		
* R2	Resistor, 1/4W 0207/8	4.7k		
* R3	Resistor, 1/4W 0207/9	470		
* U1	AY-3-8910, DIL40-6	DIL40-6 Socket Recommended		
* U2	74LS344N, DIL20	DIL20 Socket Recommended		
* U3	74LS344N, DIL20	DIL20 Socket Recommended		
* U4	74LS74N, DIL14	DIL14 Socket Recommended		
* U5	74LS30N, DIL14	DIL14 Socket Recommended		
* U6	74LS04N, DIL14	DIL14 Socket Recommended		
* U7	74LS02N, DIL14	DIL14 Socket Recommended		
* XX01	Bodge wire, ~1.25 inches, insulated 22 gauge, solid core			
* XX02	Bodge wire, ~1.0 inch, insulated 22 gauge, solid core			
* XX03	Bodge wire, ~1.75 inches, insulated 22 gauge, solid core			

## Caveats
* This project does not incorpoate any new functionality. Users who want to add this functionality may fork this project on their own.
  * SD read/write is not implemented, such as on the Micro Expander, a separate device developed by Bruce Abbott
  * RAM expansion is not included, such as the 32kb RAM Cartridge, a separate device developed by Jay Snellen, III
  * Cartridge ROM expansion is not included, such as the AquariCart, a separate device developed by Jay Snellen, III
  * Switchable use of ATARI or SEGA joysticks (despite the same DB9 plugs)
* For users who want to use RAM or ROM in either cartridge, solder jumper pads have been added to connect pin 34 (rear slot) and pin 44 (front slot) to GND. Use this at your own discretion, but understand that you can't insert two ROM cartridges and expect them to work. Two RAM cartridges have been said to work, but not sure if this is true.
* The three interconnect wires are not replaced in this stock layout. They are implemented as "WIRE" indications on the PCB which should be bridged with 22 gauge solid core, insulated wire.
* The choke/line filter (33uH) is difficult to source. Users may simply bridge this gap with 22 gauge solid core wire, or they can use a ferrite bead.
* Two of the small Control Pad interface boards are included as breakaways on either side of the narrow part of the board. These must be removed before the Mini Expander PCB will fit in the stock plastic shell. These small interface boards are used to transition the nine wires in the joystick cable to the mylar conductive pad used in the Control Pads.
