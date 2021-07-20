---
layout: post
title: Starting over
---
<a href="/viperpit/images/panels_diff_stages.jpg" border="0"><img align="right" width="320" src="/viperpit/images/panels_diff_stages.jpg" alt="Cockpit panels in progress" /></a>

With the laser cutter at hand, work started on designing new panels. This time, they would be fully modular, and each connect to a controller via it's own dupont cable.

The basic design rests on acrylic opal white 3mm panels (very good for diffusing backlight), laser cut to shape. A local shop sells these in 300x300mm, which is almost perfect for the laser cutter.

# 2D CAD

At the rear, there is a 3mm panel to hold the switches and other inputs. This is usually rectangular, and has 4mm mounting holes at the corners. The different switches will have different hole requirements - usually circular, but other shapes are easy to make with the laser cutter. Some panels also have outputs, usually with LEDS - these will be 3d-printed with acrylic diffusers and engraved text/symbols.

In front of that, a new  3mm panel creates a spacer, and additional diffusing, where the holes are a bit larger to fit washers and nuts, or other items we want to hide.

Glued on top of that is a 1mm sheet of white styrene, which will be painted black and engraved with the necessary symbols.

Both the acrylics and styrene cut files were designed [LibreCAD](https://librecad.org/) - one DXF file for the arylics per panel, and one DXF file for the styrene per panel.

TODO: Download link for all the DXF files

# Engraving

The files for engraving were designed using [Inkscape](https://inkscape.org/), in SVG format.

TODO: Download link for all the SVG files

The F-16 panels use a font called [MS33558](https://www.wfonts.com/font/ms-33558) for the most part, which I used for the engraving. One important note here: Before engraving, it is a good idea to convert all shapes to paths. This way, you are not dependent on fonts installation on all computers. It's easy to go wrong otherwise.

# Hooking up connectors
<a href="/viperpit/images/instr_wiring.jpg" border="0"><img align="right" height="320" src="/viperpit/images/instr_wiring.jpg" alt="Hookup for engine instruments" /></a>

I designed a generic PCB that holds rows of 2.54mm headers to make it easy to hook the panels up to the controllers. This is mounted on a 3D-printed bracket on the rear of the panel. Each switch is soldered to this PCB. This is a time consuming task, but well worth it when changes are needed later.

# Backlighting

For backlighting, I am not yet there. I am planning to use SMD/LED strips, that are modular. Failing that, LEDs, but that's a lot more work.

# Finished panels

<a href="/viperpit/images/panels_ready.jpg" border="0"><img width="320" src="/viperpit/images/panels_ready.jpg" alt="Cockpit panels mounted" /></a>
