
----- Fix InputStick keyboard not working on Windows 7

Problem:
 The InputStick keyboard registers itself as an HID class which
 fails to work on Windows 7

Solution:
 Force-install a 'newer' driver that adds the correct HWID of
 the InputStick keyboard device to the Keyboards class instead
 of the Human Interface Devcies class.
 
 This way you can force-update it with the modified driver as a
 Keyboard even if you cannot select the Keyboard class after it
 got installed once.

----- Steps to Fix

1. Force-install the HID driver first with dpinst64.exe
   (just move it to this folder and run it there)

2. Force-install the modded Keyboard driver with dpinst64.exe

Correct HWID to search for forcing USB Keyboard class in HWID:
- HID\VID_16D0&PID_0A75&REV_0100&MI_00
- HID_DEVICE_SYSTEM_KEYBOARD

The correct HID device must have both in its HWID properties

