---
layout: post
title: Starting over
---
<a href="/viperpit/images/in_progress_panels.jpg" border="0"><img align="right" width="320" height="246" src="/viperpit/images/in_progress_panels.jpg" alt="Cockpit panels in progress" /></a>

With the laser cutter at hand, work started on designing new panels. This time, they would be fully modular, and each connect to a controller via it's own dupont cable.

The basic design rests on acrylic opal white 3mm panels (very good for diffusing backlight), laser cut to shape. A local shop sells these in 300x300mm, which is perfect for the laser cutter. And a stern warning: *DO NOT USE polycarbonate* - which will ruin both your lungs and the laser cutter if you try jamming laser through it. 

At the rear, there is a 3mm panel to hold the switches and other inputs. This is usually rectangular, and has 4mm mounting holes at the corners. The different switches will have different hole requirements - usually circular, but other shapes are easy to make with the laser cutter. Some panels also have outputs, usually with LEDS - these will be 3d-printed with acrylic diffusers and engraved text/symbols.

In front of that, a new  3mm panel creates a spacer, and additional diffusing, where the holes are a bit larger to fit washers and nuts, or other items we want to hide. Glued on top of that is

The design of the panels were made using a couple of open source programs: [LibreCAD](https://librecad.org/) and [Inkscape](https://inkscape.org/). The former for 2D plans for the cutter in DXF format, and the latter for making engraving files in SVG format.


The F-16 panels use a font called [MS33558](https://www.wfonts.com/font/ms-33558), which I used for the engraving.

Laser cutting is a whole subject by itself. I cut the panels from (mostly) 3 layers, a bottom 3mm opal white acrylic that holds the hardware, then a new opal white 3mm layer that acts as a diffuser, as well as a distance for the hardware nuts and other fixings. Above that, a 1mm white styrene sheet that acts as a cover. This layer is glued to the middle layer, then painted black and engraved with the laser cutter for white text - which will be green when backlit. The rear layer has green LED strips attached to create the backlight. CAD files are available to create these in the cad/panels/* folders.

The dimensions for the panels are available at [hispapanels](https://hispapanels.com/tienda/en/20-f-16-fighting-falcon), where you can also buy them if you don't have access to a laser cutter. "Slightly" more expensive though. Hispapanels obviously don't give you the CAD files of course.
