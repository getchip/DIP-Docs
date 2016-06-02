
# HDMI DIP

## Intro

The HDMI DIP provides the extra hardware necessary for C.H.I.P. to output video using HDMI. To connect the DIP to C.H.I.P., first orient C.H.I.P. so that the USB connector is facing away from. Then place the DIP atop C.H.I.P. with the HDMI connector facing you and gently press the two boards together.

Using the HDMI DIP, C.H.I.P. can output a maximum resolution of X by Y at Hz.[c]

The HDMI DIP makes C.H.I.P. even better for traditional uses like presentations, classrooms, and games, and makes amazing things like [large-scale installations](http://blog.nextthing.co/this-is-how-we-made-the-75-tall-mega-pocketc-h-i-p/), magic mirrors, and [urban projection](http://c-uir.org/mup/). 

## Parts and Pieces

![HMDI top and bottom](images/hdmi_top_and_bot.jpg)

### What’s in the Bag?

There is one HDMI DIP in the electrostatic bag, packaged with protective foam.

### Pictures

![HDMI DIP Callout Graphic](images/hdmi_callout.jpg)

Callout graphic of what’s on the board

## Requirements

 * C.H.I.P. with C.H.I.P. OS 1.1 with Debian 4.4 kernel
 * HDMI display
 * HDMI cable

If you don’t have Debian 4.4, or if you are unsure, [follow this guide](#link to guide).

## Use It

![Plug it!](images/hdmi_plugged_in_half.jpg)

The HDMI DIP is extremely easy to use. Once you have your C.H.I.P. OS updated, it’s really as simple as attaching the DIP to your CHIP, plugging in an HDMI monitor, and booting up C.H.I.P. But, for posterity’s sake, here’s all the details. 

 * Connect DIP to C.H.I.P.
 * Connect cable to DIP and monitor
 * Power up C.H.I.P.


Once CHIP has power, you'll start seeing output on your monitor. Once CHIP is booted, you may want to change the resolution. You can do this with the control panel found in the Computer Things menu, going to Settings/Display 

![display control panel](images/settings_select.jpg)

In the Display control panel, you can select a resolution in the Outputs menu:

![Change Resolutions](images/settings_hdmi_resolution.jpg)

After you select a resolution, you'll need to "Apply" it:

![apply the new resolution](images/settings_apply.jpg)

If you like using commandline in the terminal, you can change resolutions with `xrandr`, such as

```shell
xrandr 1024x768
```

Supported Resolutions
HDMI DIP only does video - it does not carry an audio signal.
How to disconnect the DIP

## Open Source
HDMI DIP is open source. Design files are at github.com/etcetera

## FAQ

### Can I play HD videos on C.H.I.P.?
### How can I hear audio when I’m using HDMI?
### Can I use the composite video at the same time?