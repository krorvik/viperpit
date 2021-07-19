---
layout: post
title: Modern Simulators - back to flying
---
<a href="/viperpit/images/pre-proto2.jpg" border="0"><img align="righ" width="320" height="240" src="/viperpit/images/pre-proto2.jpg" alt="First center console" /></a>

Before the F-16 module was released, I started my DCS adventure with simple hardware: A Saitek X55 stick and throttle, and shortly after, the rather simple Thrustmaster T.Rudder pedals.

The X-55 stick is actually quite good, and matches the F-16 stick closely for button positions. It still moves of course, as it is meant for other planes too. The throttle is not as good however, and DCS does not support the multi-mode button setup. Still, a good setup for getting back into simulations.

After a while, I chose to go for an upgraded stick in the Thrustmaster HOTAS Warthog, but I did not upgrade the throttle. This is a notch up, and is more precise. And it matches the F-16 stick layout *very* well. Still, a moving stick.

# Improving a bit - prototype

At this point, I started to ponder building better panels for the F-16 consoles, to have all the inputs needed to control the DCS F-16. This would mean connecting the switches and controls via some sort of microcontroller to the PC, preferably over USB. Some searching on the internet pointed to a couple of solutions. One was the [Arduino](https://www.arduino.cc/) world, where people seemed to prefer [DCS Bios](https://github.com/DCSFlightpanels/dcs-bios) - a library well integrated with DCS, and that makes it easy to get control inputs into DCS; and data out (for dials, LEDs and such).

I also stumbled upon the [PJRC Teensy](https://www.pjrc.com/teensy/), a series of microcontrollers that also had very good libraries for USB/Joystick inputs. Additionally, DCS Bios can be adapted here with a little more (but not much) work.

The engineer in me quickly realized that this is a good project to combine my background with some more serious flying.

# Panel construction

<a href="/viperpit/images/in_progress_panels.jpg" border="0"><img align="right" width="320" height="246" src="/viperpit/images/in_progress_panels.jpg" alt="Cockpit frames in progress" /></a>

With the laser cutter, all the panels were up for a remake. The design of the panels were made using a couple of open source programs: [LibreCAD](https://librecad.org/) and [Inkscape](https://inkscape.org/). The former for 2D plans for the cutter in DXF format, and the latter for making engraving files in SVG format. The F-16 panels use a font called [MS33558](https://www.wfonts.com/font/ms-33558), which I used for the engraving.

Laser cutting is a whole subject by itself. I cut the panels from (mostly) 3 layers, a bottom 3mm opal white acrylic that holds the hardware, then a new opal white 3mm layer that acts as a diffuser, as well as a distance for the hardware nuts and other fixings. Above that, a 1mm white styrene sheet that acts as a cover. This layer is glued to the middle layer, then painted black and engraved with the laser cutter for white text - which will be green when backlit. The rear layer has green LED strips attached to create the backlight. CAD files are available to create these in the cad/panels/* folders.

The dimensions for the panels are available at [hispapanels](https://hispapanels.com/tienda/en/20-f-16-fighting-falcon), where you can also buy them if you don't have access to a laser cutter. "Slightly" more expensive though. Hispapanels obviously don't give you the CAD files of course.
