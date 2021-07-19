<a href="/viperpit/images/breakout.jpg" border="0"><img align="right" width="320" height="240" src="/viperpit/images/breakout.jpg" alt="First breakout boards" /></a>

I quickly decided on the Teensy for inputs, as at the time I did not know that the arduino/DCS Bios way was just as good. More on that later. Teensy 3.2 and 3.5 versions are used in this project.

All switches and knobs are inputs to Teensys, which are programmed as regular directx joysticks, with up to 128 buttons, and some with encoders and analog inputs from potentiometers. They are programmed so that SPST switches use one input, but are programmed to emit a button each way (OFF = button x, ON = button x + 1) - while SPDT buttons have one input and button at each end, and are programmed for an additional button in center position (both inputs off). This makes it easier to set up DCS controls.
