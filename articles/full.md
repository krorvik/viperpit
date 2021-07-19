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
