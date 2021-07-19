# First steps - the desktop center console

<a href="/viperpit/images/simple_proto.jpg" border="0"><img align="right" width="320" src="/viperpit/images/simple_proto.jpg" alt="First center console" /></a>

The first center console was really simple. A pair of acrylic class plates sandwiched a pair of 7" displaysc behind Thrustmaster cougar MFD controllers, probably at 1024x600 pixels, that overlapped towards the center.

With this, the MFDs were fully usable with image exported to the small displays. Great success!

# Input prototype

At this point, I started to ponder building better panels for the F-16 consoles, to have all the inputs needed to control the DCS F-16. This would mean connecting the switches and controls via some sort of microcontroller to the PC, preferably over USB. Some searching on the internet pointed to a couple of solutions. One was the [Arduino](https://www.arduino.cc/) world, where people seemed to prefer [DCS Bios](https://github.com/DCSFlightpanels/dcs-bios) - a library well integrated with DCS, and that makes it easy to get control inputs into DCS; and data out (for dials, LEDs and such).

I also stumbled upon the [PJRC Teensy](https://www.pjrc.com/teensy/), a series of microcontrollers that also had very good libraries for USB/Joystick inputs. Additionally, DCS Bios can be adapted here with a little more (but not much) work.

An advantage of the Teensy/DirectX route is that you do not need to match up inputs vs particular controls. You do however need to map the switches in DCS. With DCS Bios, each input must correlate to a specific input in DCS; and so is closely tied to hardware. Also note that the Teensy way means the pit can be arbitrarily mapped to other planes. Weird, but possible.

# Choosing the Teensy for inputs

<a href="/viperpit/images/breakout.jpg" border="0"><img align="right" width="320" src="/viperpit/images/breakout.jpg" alt="First center console" /></a>

At this time, I was only gunning for input controllers, and the flexible Teensy DirectX joystick library with support for 128 buttons, and many axes, made it easy to go for a first attempt. I started out with teensy 3.2 and 3.5 controllers, hooked up to a first version of a breakout board. The 3.5 has more inputs than the 3.2, and is used particularly on the busyer left console.

# Matrix switching - no go

One of my first attempt at getting more inputs out of the teensy was matrix switching. This is what is done in keyboards to support many switches with less digital inputs.

Unfortunately, there is no good way around the ghosting problems posed by this setup, so it was quickly thrown out.

# Adding inputs to the center console

<a href="/viperpit/images/early_center.jpg" border="0"><img align="right" width="320" src="/viperpit/images/early_center.jpg" alt="Second attemtp center console" /></a>

The first attempt at the center console did not have enough space for both MFDS, and some sort of ICP controller, as well as fuel switches and instrument dials. A second variant was quickly hacked together, this time with room for more inputs.

At this time, a teensy 3.5 was programmed with some digital switch inputs, and a few encoders and analog inputs (potentiometers) for the necessary switches. In addition, a small USB keyboard was hooked up as an ICP. This actually worked quite well!

# Left, right and aux consoles

# A simple rig

# Throttle solution

# New stick

Somewhere in this process, I also switched out the stick with a Thrustmaster Warthog stick. This is a good step up from the X55. A smaller base, and better stick. It does not have the correct CMDS toggle though.

# Final prototype rig
<a href="/viperpit/images/early_use2.jpg" border="0"><img align="right" width="320" src="/viperpit/images/early_use2.jpg" alt="Final prototype setup" /></a>

This is the rig as it was just before I tore it down. Seat rolls in and adjusts down, and flying commences!
