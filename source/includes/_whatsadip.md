# What's a DIP?

DIPs are accessory boards that give new capabilities to C.H.I.P.  DIPs come in many flavors, like official Next Thing Co. HDMI and VGA DIPs that give C.H.I.P. higher resolution video output to community DIPs that add more USB ports, control motors, or blink LEDs.  C.H.I.P.s (with the proper software) automatically recognize when a DIP is attached and act accordingly.

Here you'll find specs and instructions for the official Next Thing Co. HDMI and VGA DIPs as well as tips and tricks to get you started making your own.

## Requirements
To properly recognize official NTC DIPs, C.H.I.P.s will need to update to at least Debian 4.4.  For a quick start on how to update your C.H.I.P., head to [getchip.com/update](http://getchip.com/update).  Full documentation exists in the Update C.H.I.P. to Debian 4.4 section at the [bottom of the page.](#update-c-h-i-p-to-debian-4-4)

## Attaching DIPs

![Attach the DIP](images/attach.jpg)

To connect a DIP to C.H.I.P., orient the USB connector opposite the video connector. Align the pins to C.H.I.P.'s headers and gently press with even force until the two pieces are joined.

## Disconnect the DIP

With great care! It's important to pull with an even force to separate the DIP from the CHIP. You do not want bent header pins on your DIP! We've found that the [IC Extractor](https://en.wikipedia.org/wiki/IC_extractor) is an excellent companion if you want to frequently remove DIPs.