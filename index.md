---
layout: post
title:  "Ignoreme"
---
<a href="/viperpit/images/rnoaf-f-16.jpg" border="0"><img align="right" width="320" height="246" src="/viperpit/images/rnoaf-f-16.jpg" alt="RNoAF f-16AM" /></a>

As a kid, I watched one of our old [CF-104 starfighters](http://www.starfighter.no/) pass by - with another, newer, aircraft following. Some 1000ft or maybe a bit more above the fjord, they both initiated a 180 degree turn. The newer of the two had turned around long before the starfighter was even at 90 degrees.

The new aircraft was one of the Royal Norwegian Air Force F-16As, likely a block 5 or 10. Growing up less than a km away from [Vigra Airport](https://avinor.no/en/airport/alesund-airport/) AES, or ENAL, my interest for winged machines was not a strange coincident. Runway 25 started just a few meters from the road where i cycled to school, and Braathens Fokker 27 and 28s, Boeing 737 200s, and many others were watched closely by happy kid eyes at every opportunity.

Somewhere around 6th grade, possibly a bit earlier, some 6 or so vipers were forward deployed to Vigra about a week, and we could watch them closely as they danced around the sky.

The [Royal Norwegian Air Force](https://www.forsvaret.no/en/organisation/air-force) is small, and as it's only fighter jet until this year, when the [F-35](https://www.f35.com/f35/global-enterprise/norway.html) takes over, my admiration for the F-16 was only natural. Upgraded through the years, the F-16A/BM (M for MLU - Mid Life Upgrade) as it is now called is as beautiful as the block 5, and just about as capable as the modern US blocks.

Piloting a fighter jet is something few humans get to experience, and for my part, my life took me down the lanes of electronics and computers. And in this world, there are simulations. So, that was where I spent my free time. That, and building [scale models](/viperpit/images/scale.jpg).

One of the first simulations that caught my attention was Falcon 2, and if I remember it right, I played it a lot on the Amiga 500. Great fun. But of course, at this time, computing power was quite limited, and the realism you could attain was limited at best. Not to speak of graphics quality, or screen sizes.

For those of us that admire the mighty Viper, there is a hole in time where there are few choices to virtually pilot such a thing of beauty. So my interest in flight simulations - and even airplanes - was dormant for a long time. This is where the rest of life was built. Education, working, a family. And computing power.

# Modern simulators

Fast forward a few years, past 32 bit x86, pentium and 64 bit CPUs, and we're at the simulator Falcon 4.0, and the [BMS variant](https://www.benchmarksims.org/forum/content.php). The internet has taken over the world. Computers are powerful, and there is a rather good variety of commercial off the shelf controllers - by companies like Thrustmaster. Their hotas/cougar F-16 stick gave a very nice rendition of the Viper controls.

BMS is to me a very good simulator, and very specific to the F-16. It is getting a bit old though, and setup has been a little painful at times.

There are several Viper simulator pits based on Falcon BMS. Some even do custom force feedback bases for the stick. The F-16 was revolutionary on many counts, one being the sidestick controller that does not move much. Instead, the *force* applied by the pilot tells the computer what was the desired amount of control input. The computer will then decide what to do with the control surfaces.

Falcon BMS remained the choice of F-16 simpit builders for a long time (and might still be), but in 2008 another simulator hit the market, called [DCS - Digital Combat simulator](https://www.digitalcombatsimulator.com/en/index.php). It was a follow-up to a title called Lock on: Modern air combat. DCS is modular, and presents the user with a range of modules for aircraft, terrains and campaigns.

In october 2019, an [F-16C block 50 module for DCS](https://www.digitalcombatsimulator.com/en/products/planes/viper/) was released in early access. The ease of DCS install, combined with modern high quality graphics, suddenly made simulation very interesting indeed. With recent releases (2.7), DCS has become even more impressive. The module is still in early access, but is progressing nicely and becoming more complete. It has been partially overshadowed by it's F/A-18C module counterpart, but this seems to be resolving nicely now.

The hole in my simulated viper world was finally plugged.

# Getting back into simulation

<a href="/viperpit/images/pre-proto2.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/pre-proto2.jpg" alt="First center console" /></a>

Before the F-16 module was released, I started my DCS adventure with simple hardware: A Saitek X55 stick and throttle, and shortly after, the rather simple Thrustmaster T.Rudder pedals.

The X-55 stick is actually quite good, and matches the F-16 stick closely for button positions. It still moves of course, as it is meant for other planes too. The throttle is not as good however, and DCS does not support the multi-mode button setup. Still, a good setup for getting back into simulations.

After a while, I chose to go for an upgraded stick in the Thrustmaster HOTAS Warthog, but I did not upgrade the throttle. This is a notch up, and is more precise. And it matches the F-16 stick layout *very* well. Still, a moving stick.

# Improving a bit - prototype

At this point, I started to ponder building better panels for the F-16 consoles, to have all the inputs needed to control the DCS F-16. This would mean connecting the switches and controls via some sort of microcontroller to the PC, preferably over USB. Some searching on the internet pointed to a couple of solutions. One was the [Arduino](https://www.arduino.cc/) world, where people seemed to prefer [DCS Bios](https://github.com/DCSFlightpanels/dcs-bios) - a library well integrated with DCS, and that makes it easy to get control inputs into DCS; and data out (for dials, LEDs and such).

I also stumbled upon the [PJRC Teensy](https://www.pjrc.com/teensy/), a series of microcontrollers that also had very good libraries for USB/Joystick inputs. Additionally, DCS Bios can be adapted here with a little more (but not much) work.

The engineer in me quickly realized that this is a good project to combine my background with some more serious flying.

# Hardware choice for inputs

<a href="/viperpit/images/breakout.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/breakout.jpg" alt="First breakout boards" /></a>

I quickly decided on the Teensy for inputs, as at the time I did not know that the arduino/DCS Bios way was just as good. More on that later. Teensy 3.2 and 3.5 versions are used in this project.

All switches and knobs are inputs to Teensys, which are programmed as regular directx joysticks, with up to 128 buttons, and some with encoders and analog inputs from potentiometers. They are programmed so that SPST switches use one input, but are programmed to emit a button each way (OFF = button x, ON = button x + 1) - while SPDT buttons have one input and button at each end, and are programmed for an additional button in center position (both inputs off). This makes it easier to set up DCS controls.

# Realistic panels

<a href="/viperpit/images/final-proto.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/final-proto.jpg" alt="Final prototype" /></a>

I continued building a "center console", with Thrustmaster Cougar Multifunction displays, mounted on an acrylic glass plate, a 7" LCD panel per MFD; and a center mini USB keyboard for ICP input. This was my first attempt at using acrylics for making panels.  

Slowly improving, I build left and right consoles using wooden consoles (onepiece) with acrylic panels (separate), and labels printed with a Dymo labelmaker. Black model acrylic paint and matte clear laquer finished the job. I even built a throttle with a 3d-printed grip ([Viper Pitstop @ shapeways ](https://www.shapeways.com/shops/f16)) for a more realistic feel. The results were not bad at all.

Switches were micro chinese, cheap and unreliable, but could easily be replaced, as I ordered them in batches of 100. Simple breakout PCBs were made for the Teensys, and the switches had dupont headers on prototype PCBS to hook them up to the breakout boards.

I also experimented with switch matrixes for the inputs, but the (known) problems with matrixes and ghosting made them impossible to use, so I reverted to one input per switch function.

The full frame was made so my office chair could be lowered and placed in the center, while the center console was hinged and could be stowed while I used my computer for other purposes. Like work - financing the thing ;)

Things were quite good, I could now fly without using the mouse or keyboard.

# Current status

<a href="/viperpit/images/status.jpg" border="0"><img align="right" width="240" height="320" src="/viperpit/images/status.jpg" alt="status" /></a>

At the moment, some outputs are still missing, and there is still center console work to do, but I include this image for a quick view.

# DevOps

[DevOps](https://en.wikipedia.org/wiki/DevOps) in computer science is the art of developing software with continuous improvement, and making small, controlled changes as you go. It is in my nature to keep going. At this point, a few weaknesses were apparent:

* Cable spaghetti - a lot of dupont wiring and USB cables.
* Moving sidestick
* Center console not quite well shaped
* No instruments or lights (outputs) - only inputs
* Not really a good representation of panels (only crude positioning)
* Joystick where right aux panel should be
* Throttle a bit lacking

# Tools of the trade

For christmas in 2020, my wife gave me an Ender 3 3d-printer. A little before that, I gained access to a 40W  laser cutter with a sufficient cutting area to cut parts around 30x20cm.

These are excellent tools to make panels, and print other needed parts for a cockpit. So I started the journey to a new and improved pit. The following sections describe the journey.

# New switches

I chose to use more realistic switches this time around - heavy duty SPST and SPDT switches, latching or momentary where needed. These are also of chinese origin, but not quote as cheap as the small ones used before. In some locations more expensive switches with a small body are used due to space reuqirements.

# Panel construction
<a href="/viperpit/images/in_progress_panels.jpg" border="0"><img align="right" width="320" height="246" src="/viperpit/images/in_progress_panels.jpg" alt="Cockpit frames in progress" /></a>

With the laser cutter, all the panels were up for a remake. The design of the panels were made using a couple of open source programs: [LibreCAD](https://librecad.org/) and [Inkscape](https://inkscape.org/). The former for 2D plans for the cutter in DXF format, and the latter for making engraving files in SVG format. The F-16 panels use a font called [MS33558](https://www.wfonts.com/font/ms-33558), which I used for the engraving.

Laser cutting is a whole subject by itself. I cut the panels from (mostly) 3 layers, a bottom 3mm opal white acrylic that holds the hardware, then a new opal white 3mm layer that acts as a diffuser, as well as a distance for the hardware nuts and other fixings. Above that, a 1mm white styrene sheet that acts as a cover. This layer is glued to the middle layer, then painted black and engraved with the laser cutter for white text - which will be green when backlit. The rear layer has green LED strips attached to create the backlight. CAD files are available to create these in the cad/panels/* folders.

The dimensions for the panels are available at [hispapanels](https://hispapanels.com/tienda/en/20-f-16-fighting-falcon), where you can also buy them if you don't have access to a laser cutter. "Slightly" more expensive though. Hispapanels obviously don't give you the CAD files of course.

# Pit frame construction

<a href="/viperpit/images/in_progress_pit_frame.jpg" border="0"><img align="right" width="240" height="320" src="/viperpit/images/in_progress_pit_frame.jpg" alt="Cockpit frames in progress" /></a>

<a href="/viperpit/images/in_progress_pit1.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/in_progress_pit1.jpg" alt="Cockpit frames in progress" /></a>

The pit itself was rebuilt, this time with a more correct overall shape (although not precise).

The panels are not mounted directly to the pit, but on separate panel mounting frames that attach to the pit.

The pit frame itself is divided into sections - the rear left console, front left console, left auxiliary console, right auxiliary console, and right console (not split). For the left and right side consoles, the frame is angled 7 degress towards the seat. Construction is done using 23x30mm wood cut using a precise table saw. I'd advise against manual cuts.

The floor is a separate part, with the pedal part protruding in front of the center console position, and the seat part sloping down towards the back to support an angled seat (The actual F-16 ACES-II seat back is reclined 30 degrees).

In front of the center console, a more solid frame built from 48c98mm wood is placed to support a large TV screen.

# Panel mounting frames

# Center console frame

# New sidestick and mount

# Panel mounts

# Controller setup - inputs

## switches

## potentiometers

## Encoders

## Side wall inputs

# Controller setup - outputs

## LED based

### Caution panel

### Indexers

### Eyebrow lights and master caution

### Left console status and warning lights

### UHF panel
<a href="/viperpit/images/in_progress_uhf.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/in_progress_uhf.jpg" alt="UHF panel test" /></a>

## Rotary instruments

# Landing Gear lever

# Bass shaker

# Throttle design
<a href="/viperpit/images/in_progress_throttle.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/in_progress_throttle.jpg" alt="Throttle assy" /></a>
# Rudder pedals

# ICP

# Seat

# Screen
