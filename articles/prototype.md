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

Next, the main consoles were built. For the left console, a wooden frame was built, upon which switches etc was mounted, and then simple 4mm acrylic sheets painted black, and labeled with a labelmaker, was placed on top to simulate the panels. For the left aux console and the right consoles, acrylic sheet was chosen for both layers.The images attached show these:

<a href="/viperpit/images/early_wood_console.jpg" border="0"><img width="320" src="/viperpit/images/early_wood_console.jpg" alt="Consoles" /></a>
<a href="/viperpit/images/early_console.jpg" border="0"><img width="320" src="/viperpit/images/early_console.jpg" alt="Consoles" /></a>
<a href="/viperpit/images/early_console_painted.jpg" border="0"><img width="320" src="/viperpit/images/early_console_painted.jpg" alt="Consoles" /></a>
<a href="/viperpit/images/early_laux.jpg" border="0"><img width="320" src="/viperpit/images/early_laux.jpg" alt="Consoles" /></a>
<a href="/viperpit/images/early_right_console.jpg" border="0"><img width="320" src="/viperpit/images/early_right_console.jpg" alt="Consoles" /></a>

# Throttle solution no 1
<a href="/viperpit/images/early_throttle.jpg" border="0"><img align="right" width="320" src="/viperpit/images/early_throttle.jpg" alt="Early throttle" /></a>

I decided to hack up the X55 throttle, and used the mechanism itself together with a lengthened handle to create something a bit more realistic. Still a stretch, but a bit easier on the hands ;)

# Throttle solution no 2

I spent some time looking for a good way to replicate the throttle handle. I ended up getting a 3D-printed shell of it from Shapeways. Filled with resin, and then with hardware added - it made a good first attempt at a real throttle grip. 

# New stick

Somewhere in this process, I also switched out the stick with a Thrustmaster Warthog stick. This is a good step up from the X55. A smaller base, and better stick. It does not have the correct CMDS toggle though.

# Final prototype rig

<a href="/viperpit/images/early_rig.jpg" border="0"><img width="320" src="/viperpit/images/early_rig.jpg" alt="Early prototype rig" /></a>
<a href="/viperpit/images/early_use2.jpg" border="0"><img width="320" src="/viperpit/images/early_use2.jpg" alt="Final prototype setup" /></a>

The early rig was very simple, wooden frames that the consoles were mounted onto. The idea was to lower the chair and roll it into the pit, so to speak. Then fly!
