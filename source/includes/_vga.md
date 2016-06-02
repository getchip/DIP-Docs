# VGA DIP

## Intro

The VGA DIP allows C.H.I.P. to connect to a monitor via a standard 9-pin VGA cable at a maximum output resolution of 1600 by 900 at 60 Hz. Unlike the 16:9 ratio of HDMI, the VGA DIP outputs in a 4:3 aspect ratio.

## Parts and Pieces

![VGA top and bottom](images/vga_top_and_bot.jpg)

### What’s in the Bag

There is one VGA DIP in the electrostatic bag, packaged with protective foam.
VGA cables and C.H.I.P.s are sold separately [at getchip.com](https://getchip.com/pages/store)

### Pictures

![VGA DIP Callout Graphic](images/vga_callout.jpg)

 * RGB breakouts - RGB breakouts can be found at the edge of the VGA connector on the left side. These are available if you ever want to add cool effects, or to “bend” your VGA DIP
 * Trim-pot breakouts (RGB) - There are three footprints for1 0K trimpots. These can be installed with only a few solder joints, and can create a really awesome visual effects like saturating colors.
 * U14 breakouts - The U14 header breakout is directly to the left of U14. This is important if you would like to access FEL, UART, XIO, CSID, audio, etc. The name of each pin is labeled above the corresponding pad.
 * JST connector breakout - A JST connector footprint  is available to be populated on VGA DIP. Because the VGA connector is really close to the existing JST battery connector, it makes it difficult to plug/unplug with the VGA DIP installed. Note: DO NOT INSTALL TWO BATTERIES INTO C.H.I.P. THIS WILL DAMAGE YOUR C.H.I.P. 
 * Prototyping area - There is “Proto board” on the PCB itself. This is convenient if you would like to add a small circuit to your VGA DIP, without having to add another board.
 * VGA connector - This is a standard female DB-15 VGA connector to carry the video signal to a VGA monitor. 
 * Power switch - A Power switch has been added to the VGA DIP. It is close to impossible to access the Power On Switch on C.H.I.P with the VGA DIP installed, so we added a second Power On Switch. This is located on the right side of the PCB, and is accompanied by a “Power On” symbol. 

## Requirements

 * C.H.I.P. with C.H.I.P. OS 1.1 with Debian 4.4 kernel
 * VGA display
 * VGA cable (we recommend a cable with Ferrite beads)
If you don’t have Debian 4.4, or if you are unsure, [follow this guide](getchip.com/update)

## Use It

The VGA DIP is extremely easy to use. Once you have your C.H.I.P. OS updated, it’s really as simple as attaching the DIP to your C.H.I.P, plugging in a VGA monitor, and booting up C.H.I.P. But, for posterity’s sake, here’s all the details. 

 * Update C.H.I.P. OS
 * Connect DIP to C.H.I.P.
 * Connect cable to DIP and monitor
 * Power up C.H.I.P.

Once C.H.I.P has power, you'll start seeing output on your monitor. Once C.H.I.P is booted, you may want to change the resolution. You can do this with the control panel found in the Computer Things menu, going to Settings/Display 

![display control panel](images/settings_select.jpg)

In the Display control panel, you can select a resolution in the Outputs menu:

![Change Resolutions](images/settings_vga_resolution.jpg)

After you select a resolution, you'll need to "Apply" it:

![apply the new resolution](images/settings_apply.jpg)

If you like using commandline in the terminal, you can change resolutions with `xrandr`, such as

```shell
xrandr -s 1024x768
```

## Know It

### Supported Resolutions

We cannot provide an exhaustive list of all resolutions, since this can depend on the attached monitor, but here are some observed resolutions:

  * 1600x900
  * 1280x1024
  * 1152x864
  * 1024x768
  * 800x600
  * 640x480
  * 720x400


### How to disconnect the DIP

With great care! It's important to pull with an even force to separate the DIP from the CHIP. You do not want bent header pins on your DIP! We've found that the [IC Extractor](https://en.wikipedia.org/wiki/IC_extractor) is an excellent companion if you want to frequently remove DIPs.

## Hack It

Heat up your soldering iron, the VGA DIP is hackable. You may have noticed the pads suitably spaced for 10K trim pots, and the RGB breakouts. Here's a photo guide to soldering up some trim pots so you can manually adjust the individual red, green, and blue levels in the image.

![Through hole application](images/vgapot_01thruhole.jpg)

![Place the pots](images/vgapot_02place.jpg)

![Solder the pots to the VGA board](images/vgapot_03soldered.jpg)

![Control and compose](images/vgapot_04allpots.jpg)

## Open Source

VGA DIP is open source. Design files are in our [github repo.](https://github.com/NextThingCo/VGA_DIP)

## FAQ

Can I play HD videos on C.H.I.P.?
Can I use the composite video at the same time?

