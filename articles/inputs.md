---
layout: post
title: Teensy input design
next: throttle
previous: commercial
---

<a href="/viperpit/images/breakout.jpg" border="0"><img align="right" width="320" src="/viperpit/images/breakout.jpg" alt="Teensy boards, early version" /></a>

NOTE: This page needs more work, as it is written without access to the sketch files. It will be expanded!

All the DIY input controllers are based on a Teensy controller. Inputs are used as follows:

* 2 digital inputs per encoder
* 1 digital input per SPST switch, mapped to 2 buttons/positions
* 2 digital inputs per SPDT switch, mapped to 3 buttons
* 1 Analog input per potentiometer

# Breakout board and pin use

I designed an easy breakout board for the 3.2 and 3.5, that you can download and use freely. Note that the matrix boards to the left were rejected due to ghosting issues. They would only really be useful for momentary functions.

These boards assume:

* 3.2: Pins 0 - 34 are used for digital inputs
* 3.2: Pins A0-A4 are used for analog potmeters
* 3.5; Pins 0-53 are used for digital inputs
* 3.2: Pins A0-A5 are used for analog potmeters

You may also set a number of encoders for each teensy, these will use pins 0 - 2 x encoder_count

In addition, the sketch allows for selecting which digital pins should NOT emit a second button for rotary switches, and which are the two pins of a SPDT button - and should emit *tree* buttons. Note that three-position rotary buttons may be connected with two pins (center unconnected), and programmed as a SPDT, The comments explain this in detail.

TODO: Download gerber files or eagle files

# Teensy sketches

You need to [learn how to program the teensy](https://www.pjrc.com/teensy/tutorial.html) before continuing on this page.

# Setup

We are using the teensy as a USB HID device, so we have to program each device with a separate PRODUCT_ID (or VENDOR_ID, but prefer PRODUCT_ID). I have included a modified usb_desc.h file here, that needs to be placed in the original location on your hard drive. Modify this file as noted for each teensy device before compiling the sketch. There are commented sections for each teensy I've used:

* L_aft (3.5)
* L_fwd (3.5)
* Centr (3.5)
* Thrtl (3.2)
* R_fwd (3.2)
* R_aft (3.2)

You may only program one teensy at a time without additional tools, and I suggest keeping only one connected at a time while programming and setting up.

# The sketch

The basic sketch is the same for all devices. There is a a section at the top that must be modified for each device. Start by compiling and uploading the file unchanged.

Then connect it as you expect it to the switches, and use a joystick testing tool to note which buttons need to have special handling (SPDTs, rotary switches). You do not need to map anything about regular SPSTs or momentary push buttons.

Then modify the code, and reprogram the teensy. The changed witches should now act according to comments in the code.
