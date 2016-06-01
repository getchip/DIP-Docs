# What’s a DIP?

DIPs are accessory boards that attach directly to C.H.I.P. and add extra hardware capabilities. For example, the HDMI DIP and VGA DIP both output specialized video formats that C.H.I.P. could not do without the additional DIP hardware. 
DIPs come in all sorts of flavors. -- from officially Next Thing Co. DIPS like the HDMI and VGA accessory boards to community created DIPS that increase the number of USB ports on C.H.I.P. or control motors and LED matrices. [a]While any C.H.I.P.-attached hardware can be casually called a DIP, for an accessory board to be officially be called a DIP, it must adhere to the C.H.I.P. DIP Specification[b]..

# HDMI DIP

## Intro

The HDMI DIP provides the extra hardware necessary for C.H.I.P. to output video using HDMI. To connect the DIP to C.H.I.P., first orient C.H.I.P. so that the USB connector is facing away from. Then place the DIP atop C.H.I.P. with the HDMI connector facing you and gently press the two boards together.

Using the HDMI DIP, C.H.I.P. can output a maximum resolution of X by Y at Hz.[c]

The HDMI DIP makes C.H.I.P. even better for traditional uses like presentations, classrooms, and games, and makes amazing things like [large-scale installations](http://blog.nextthing.co/this-is-how-we-made-the-75-tall-mega-pocketc-h-i-p/), magic mirrors, and [urban projection](http://c-uir.org/mup/). 

## Parts and Pieces

![HDMI top](images/HDMI_top.png)
![HDMI bottom](images/HDMI_bottom.png)

### What’s in the Bag?

There is one HDMI DIP in the electrostatic bag, packaged with protective foam.

### Pictures

![HDMI DIP Callout Graphic](images/hdmi_callout.png)
Callout graphic of what’s on the board

## Requirements

 * C.H.I.P. with C.H.I.P. OS 1.1 with Debian 4.4 kernel
 * HDMI display
 * HDMI cable

If you don’t have Debian 4.4, or if you are unsure, [follow this guide](#link to guide).

## Use It

Connect DIP to C.H.I.P.
Connect cable to DIP and monitor
Power up C.H.I.P.
Change resolutions with Computer Things/Settings/Display control panel
Change resolutions with xrandr in command line
Supported Resolutions
HDMI DIP only does video - it does not carry an audio signal.
How to disconnect the DIP

## Open Source
HDMI DIP is open source. Design files are at github.com/etcetera

## FAQ

### Can I play HD videos on C.H.I.P.?
### How can I hear audio when I’m using HDMI?
### Can I use the composite video at the same time?

# VGA DIP

## Intro

The VGA DIP enables C.H.I.P. to output a video signal over a standard 9-pin VGA cable. To connect the DIP to C.H.I.P., first orient C.H.I.P. so that the USB connector is facing away from. Then place the DIP atop C.H.I.P. with the VGA connector facing you and gently press the two boards together[d].  

The VGA DIP supports higher resolutions than the on-board composite video output, with a maximum output resolution of TK by TK at TK Hz[e]. Additionally, the VGA DIP outputs resolutions in a 4:3 aspect ratio.

## Parts and Pieces
![VGA top](images/vga_top.png)
![VGA bottom](images/vga_bottom.png)

### What’s in the Bag

There is one VGA DIP in the electrostatic bag, packaged with protective foam.

### Pictures

![VGA DIP Callout Graphic](images/vga_callout.png)

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
The VGA DIP is extremely easy to use. It’s really as simple as attaching the DIP to your CHIP, plugging in a VGA monitor, and booting up CHIP. But, for posterity’s sake, here’s all the details. 

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

# DIP DIY
Specification https://w.nextthing.co/doku.php?id=dip_specification
DIP Developer’s Kit https://w.nextthing.co/doku.php?id=dip_developers_kit

# Updating C.H.I.P. to Debian 4.4
In addition to being physically attached to C.H.I.P., DIPs require that C.H.I.P. is running the Debian 4.4 Linux kernel.
Determine C.H.I.P.’s Kernel Version
To determine if you need to upgrade your C.H.I.P.’s kernel, connect a keyboard, mouse, and display to C.H.I.P., then power on the board. 
Once open the terminal application from the drop-down menu at the top, left corner of the Desktop.

Once the applications loads, type `uname -a`. This outputs information about your system software version. 
Look for a number in appended with `-ntc`, for example `4.3.0-ntc` or `4.4.0-ntc`. This number is the kernel version running on your C.H.I.P. If the number is `4.4.0` or greater, you don’t need to upgrade your kernel version. If your number is `4.3.0`, keep reading, you need to upgrade your kernel.

## Back-up C.H.I.P.’s Data
Back-up any important data on your C.H.I.P. before you upgrade your system. Upgrading will overwrite all of the C.H.I.P. storage.

## Upgrade the Kernel with the C.H.I.P. Flasher

Using the [Chrome](https://www.google.com/chrome/browser/desktop/) or [Chromium](https://www.chromium.org/getting-involved/download-chromium) web browser, visit [flash.getchip.com](http://flash.getchip.com) and follow the on-screen instructions. When the flasher presents you with different OS images to choose from, click on “CHIP OS 1.1” to select it.

When flashing is complete, follow the instructions for using your DIP.
