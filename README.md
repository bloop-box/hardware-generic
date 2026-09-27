# How to build a Bloop-Box

This repository describes the general needs to build the Bloop-Box hardware

## What you need for each box

- The three boards (Mainboard, Tailboard, LED-Board)
- Case
- Power Supply
- Speaker
- Raspberry Pi Zero 2 W with header pins
- NFC-Reader
- Cables
- RGB-LED
- some screws depening on your case design 

### Raspberry Pi

The best choice is the Raspberry Pi Zero 2 W since it is small form factor and uses less power than the bigger ones. The Zero 1 does not work since it has no 64 bit support. 

Any other Raspberry Pi that supports a 64 bit OS should work as well but keep in mind that you need a much bigger case for those and also might have to use a bigger power supply. 

The Raspberry Pi also needs the standard make header pins to connect the Mainboard to it.

### NFC-Reader

The reader we use in our boxes is a cheap and common board named "RFID-RC522" - looking that up should give you the correct one since it is a very common part for use with Raspberry Pi and microcontrollers. 

You can see the needed pinout in the documentation of the Mainboard. Most important is the used chipset - another chip would mean a rewrite of the client software. If the pinout of your reader is different you will have to adapt with the cable. 

### Cables

You need some cables for the internal connections. Everything uses cheap JST PH compatible connectors. The NFC-reader uses a JST XH compatible connector because of the wider hole spacing.

All cables are connected 1:1 

- 4 pin JST PH to PH cable for the LED-Board
- 8 pin JST PH to PH cable for the Tailboard
- 8 pin JST PH to XH cable for the NFC-Reader
- 2 pin JST PH cable for the speaker

### Power supply

We use the original Raspberry Pi 4 power supply for our boxes since it is stable and has a USB-C plug already but any power supply that delivers stable 5V with at least 2A should be fine. 

### Speaker

Any generic 4Ω 3W speaker will do. We use 2" speakers in our boxes. Just make sure it is a full spectrum speaker to get proper sound out of it. 

### RGB-LED

The LED-Board needs the LED soldered in after delivery. Use any standard 5mm Common Anode RGB-LED. Do *not* use Neopixels or similar - just a dumb LED. 

LEDs with opaque casings are preferred unless you want to put your own diffuser on top. 
