# Fix InputStick for Windows 7
Fix the InputStick keyboard not working in Windows 7 in HID class (force Keyboard class).
Fixed using modified HIDInput & Keyboard drivers (actually just some INF file edits).

## What is this for?
It's made for the [InputStick.com USB receiver](http://inputstick.com/) which otherwise only works as a mouse on Windows 7 due to a bug in its HID keyboard class handling.

You likely don't need this if you don't own the physical InputStick device.\
However if you do have it & run Windows 7, then you will finally be happy to make it work with your older OS.

## I have it, how to install this?
Just move the dpinst64.exe file to the **1 - HID Driver** folder first then run it to install the drivers.\
The drivers are unsigned due to the INF file edits for InputStick support, accept the unsigned driver install.

Now do the same again and move dpinst64.exe to the **2 - Keyboard Driver** folder and run it again there.\
Accept the unsigned driver install once again to complete the install process.

Now use the **readme.txt** and read how to locate the faulty InputStick HID device in your Device Manager (devmgmt.msc).\
Force-update it with the "InputStick HID Keyboard" entry (any of the two items, doesn't matter) to switch it into a Keyboard class device.

## More info
I currently made this for 64-bit Windows 7 only, I don't have a 32-bit Windows 7 OS to take original files from.
I could do it for 32-bit too someday.
