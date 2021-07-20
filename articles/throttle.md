---
layout: post
title: Throttle design
next: outputs
previous: inputs
---

The throttle in the F-16 is one of the interesting design points. The throttle rotates normally around a center, but the rod the grip is attached to is curved, and a hinged grip slots, via an extension, into a rail on the sidewall. There is also an "idle detent" with a special handle on the grip base that releases the grip from off to idle.

This is a challenge, but clearly a job for a 3D-printer!

# Thrustmaster TQS

<a href="/viperpit/images/tqs.jpg" border="0"><img align="right" width="320" src="/viperpit/images/tqs.jpg" alt="Oldie but goodie" /></a>

Back in the day Thrustmaster had a design called the "F-16 TQS", that had the correct grip, but the handle and base was way off. The grip, however, was really good - so much in fact, that it is almost a 1:1 replica. The only problem is that most of them come with a really strange cursor control. It was also a serial design, and did not have USB.

But all this is fixable, as the grip itself can be detached and modified. Let's go.

# Teensy controller

The throttle has it's own teensy, and is programmed a little differently - the throttle potentiometer only travels part of it's range, and needs to emit idle/cutoff buttons, and start it's curve after detent passage. The AB detent will be purely mechanical, so does not need programming.

# Get a grip

Hehe. I found a TQS with an F-22 stick on a local web second hand market, so I promptly bought it. Splash one. Detach grip, throw away stick.

# Design the rest

<a href="/viperpit/images/throttle_mount.jpg" border="0"><img align="right" width="320" src="/viperpit/images/throttle_mount.jpg" alt="Throttle mount, no rail" /></a>

I used tinkercad, a really nice online 3D-designer, to construct several parts:

* A handle that accepts a potentiometer in the rotational center, that bends inwards at about the right curve
* A connector for the grip base on that handle, that rotates for idle/mil/ab detents
* A grip base that attaches to that and the grip itself
* A mount for the sidewall that holds the handle and the rail the grip assy slides along

Sounds simple, right? Well... it took a few tries.

# Throttle mount

The throttle mount consists of two parts, one part that attaches to the console and panel frames on the left console, and one part that attaches
to the other one when the handle is attached, and the potentiometer inserted in the middle of the handle "center".

The main throttle potentiometer is attached to the inner part, in the center of handle attachment.

TODO: Download STLs

# Handle

The handle is two parts, the first is the rotating center, with a center pot hole (hehe), and a protruding cylinder around that that slots into the throttle mount.

The second part is the adapter for the grip base, and attaches to the grip end, and is glued and screwed securely in place.

TODO: Download STLs

# Grip

<a href="/viperpit/images/grip.jpg" border="0"><img align="right" width="320" src="/viperpit/images/grip.jpg" alt="Disassembled grip" /></a>

The main grip is from the TQS, and attaches to the grip base via an adapter that fits the "nut slots" in the grip.

The grip itself is stripped of all cables, and potentiometers are replaced with new ones. The range pot needs to have a push momentary switch in addition to the pot. Also, the cursor was the old type, so I replaced it with an alps four way switch with center momentary push button that i designed a box to hold it in place in the mount the old cursor used.

I used one of the panel dupont boards to create a stable connection for dupont cables running through the center-holed handle to the throttle teensy mounted in the side console. The main throttle potentiometer is mounted on the throttle base, and has a separate connection to the controller

TODO: Download STLs

# Rail design

The rail prints in two parts, front and rear, and attaches to the throttle mount on each side. The front and rear parts have couplers that make a strong attachment.

TODO: Download STLs
