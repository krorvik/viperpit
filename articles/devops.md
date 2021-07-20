---
layout: post
title: Continous improvement
next: tools
previous: prototype
---
<a href="/viperpit/images/early_spaghetti2.jpg" border="0"><img align="right" width="320" src="/viperpit/images/early_spaghetti2.jpg" alt="Room for improvement" /></a>

[DevOps](https://en.wikipedia.org/wiki/DevOps) in computer science is the art of developing software with continuous improvement, and making small, controlled changes as you go. I've worked this way for many years, and the methods we use are very much applicable to other subjects.

It is in my nature to keep going. At this point, a few weaknesses were apparent:

* Cable spaghetti - a lot of dupont wiring and USB cables.
* Moving sidestick
* Center console not quite well shaped
* No instruments or lights (outputs) - only inputs - still need to see rendered pit for info
* Not really a good representation of panels (only crude positioning)
* Stick where right aux panel should be
* Throttle still a bit lacking, and not quite precise

This, of course, is a perfect reason to spend another year (?) at the workbench, improving the pit.

# Planned improvements

Some of the important improvements were, not in priority order:

* Better visual quality for panels
* New console frames
* New seat
* Better hardware (switches, pots)
* Add outputs for instruments and indicators, using Arduinos and DCS Bios
* Force feedback stick (yeah)
* New throttle with idle and AB detents
* Cleaner wiring
* Bass shaker under seat (Ground/Taxi shaking, weather, buffeting)

# Rules

Some rules are nice to follow:

* Panels must be modular, and should unmount and disconnect easily
* All inputs are via Teensys, mapped in the game.
* All switch inputs should emit buttons in each position
* All outputs are via Arduinos on DCS Bios, on a RS485 bus
* Stepper motors should be used for rotary instruments
