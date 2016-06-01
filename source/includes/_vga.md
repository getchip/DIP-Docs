# VGA DIP

## Intro

The VGA DIP enables C.H.I.P. to output a video signal over a standard 9-pin VGA cable. To connect the DIP to C.H.I.P., first orient C.H.I.P. so that the USB connector is facing away from. Then place the DIP atop C.H.I.P. with the VGA connector facing you and gently press the two boards together[d].  

The VGA DIP supports higher resolutions than the on-board composite video output, with a maximum output resolution of TK by TK at TK Hz[e]. Additionally, the VGA DIP outputs resolutions in a 4:3 aspect ratio.

## Parts and Pieces
![VGA top and bottom](images/vga_top_and_bot.jpg)

### What’s in the Bag

There is one VGA DIP in the electrostatic bag, packaged with protective foam.

### Pictures

![VGA DIP Callout Graphic](images/vga_callout.jpg)

 * RGB breakouts - RGB breakouts can be found at the edge of the VGA connector on the left side. These are available if you ever want to add cool effects, or to “bend” your VGA DIP
 * Trim-pot breakouts (RGB) - There are three footprints for trimpots, which can be found [here]. These can be installed with only a few solder joints, and can create a really awesome visual effects like saturating colors.
U14 breakouts - The U14 header breakout is directly to the left of U14. This is important if you would like to access FEL, UART, XIO, CSID, audio, etc. The name of each pin is labeled above the corresponding pad.
 * JST connector breakout - A JST connector footprint  is available to be populated on VGA DIP. Because the VGA connector is really close to the existing JST battery connector, it makes it difficult to plug/unplug with the VGA DIP installed. Note: DO NOT INSTALL TWO BATTERIES INTO CHIP. THIS WILL DAMAGE YOUR CHIP. 
 * Prototyping area - There is “Proto board” on the PCB itself. This is convenient if you would like to add a small circuit to your VGA DIP, without having to add another board.
 * VGA connector - The VGA connector. This is a standard female DB-15 VGA connector to carry the video signal to a VGA monitor. 
 * Power on switch - A Power On Switch has been added to the VGA DIP as well. It is close to impossible to access the Power On Switch on C.H.I.P with the VGA DIP installed, so we added a second Power On Switch. This is located on the right side of the PCB, and is accompanied by a “Power On” symbol. 

## Requirements
 * C.H.I.P. with C.H.I.P. OS 1.1 with Debian 4.4 kernel
 * VGA display
 * VGA cable (we recommend a cable with Ferrite beads)
If you don’t have Debian 4.4, or if you are unsure, [follow this guide](getchip.com/update)

## Use It
The VGA DIP is extremely easy to use. Once you have your C.H.I.P. OS updated, it’s really as simple as attaching the DIP to your CHIP, plugging in a VGA monitor, and booting up CHIP. But, for posterity’s sake, here’s all the details. 

Update C.H.I.P. OS
Connect DIP to C.H.I.P.
Connect cable to DIP and monitor
Power up C.H.I.P.
Change resolutions with Computer Things/Settings/Display control panel
Change resolutions with xrandr in command line
Supported Resolutions

## Hack It
Heat up your soldering iron, the VGA DIP is hackable. Add pots to adjust RGB
trim pots vs. regular pots
Use CHIP GPIO to turn RGB channels on/off

## Open Source
VGA DIP is open source. Design files are at https://github.com/NextThingCo/VGA_DIP
FAQ
Can I play HD videos on C.H.I.P.?
Can I use the composite video at the same time?
