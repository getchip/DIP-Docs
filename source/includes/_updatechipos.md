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
