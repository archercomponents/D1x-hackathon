# D1x-hackathon
General information about how to interact with the D1x Trail shifting system via BLE

The D1x Trail Electronic Shifter uses Bluetooth Low Energy to connect to the Archer app and to the remote. This repo is intended to provide basic information about how to interact with the system via BLE using a 3rd party connection device.

There are a lot of things you can do with this info so be careful and don't go touching characteristics that you don't understand. Shit can go sideways in a hurry. If you have questions or don't see something you need, contact us at support@archercomponents.com and we'll do what we can to support your hackery. 

Oh, and since this goes beyond the normal use of our devices, altering BLE data can lead to voiding the warranty on your device. Just saying, be careful.

Okay, on to the good stuff.

The shifter is a BLE peripheral device. The remote is a BLE central device. The app is a BLE central device.

The shifter can only connect to either the remote or the app, not both simultaneously. Also, when the shifter is connected to the remote, you can't break into that communications link with the app - this is by design - we don't want anyone interupting your ride without your express permission. 

Shifter LED - red blinking: broadcasting name "D1x-aabbcc" at full power and searching for central device to connect to.
Shifter LED - green blinking: connected to central device. (if device is app, shifter will not go into sleep mode. If device is remote, shifter goes into sleep mode 10 seconds after last shift or button click - PWM output signal is cut off sending motor into deep sleep as well.
