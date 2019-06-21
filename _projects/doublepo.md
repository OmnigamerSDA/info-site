---
title: Double Punch-Out!!
subtitle: One Controller, Two Consoles
layout: page
icon: fa-hand-rock
order: 4
---
<span class="image left"><img src="{{ 'assets/images/doublepo_box.jpg' | relative_url }}" alt="" /></span>Before game submissions to AGDQ 2018, runner zallard1 asked me if it was possible to make a device that would allow one controller to provide inputs to a NES and SNES simultaneously. The goal was to allow playing both Mike Tyson's Punch-Out!! (NES) and Super Punch-Out!! (SNES) simultaneously. I was fresh off of setting up MashAttack, so I was plenty familiar with handling the controller inputs, and it seemed straightforward enough. The core idea was to have a microcontroller act as an intermediary between the player's controller and both consoles.

However, working with two distinct consoles provided some unique challenges. First, each console had its own clock. Nominally they should have been the same frequency, but in reality there will always be some drift over time that could create race conditions. Not only that, but since the clocks start relative to power-on, they will be out-of-phase. This all boiled down to one solution: updates out to the consoles needed to be non-blocking, or sufficiently fast.

<blockquote class="twitter-tweet tw-align-center"><p lang="en" dir="ltr">For science&#13;&#13;Also for punching stuff <a href="https://t.co/HkwNHzJj3Z">pic.twitter.com/HkwNHzJj3Z</a></p>&mdash; Omnigamer (@TheOmnigamer) <a href="https://twitter.com/TheOmnigamer/status/920525304300474368?ref_src=twsrc%5Etfw">October 18, 2017</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

The second issue was translating the player's controller inputs into compatible inputs for each console. The controller protocols for NES and SNES are very similar; NES uses one data byte while SNES uses two. The actual button mappings were arbitrary - I simply applied one-to-one mappings of SNES buttons to NES buttons in the data bytes, according to zallard's requirements. I used dedicated SPI controllers to transfer the data out so it wouldn't block the main processor from polling.

The end result worked! Well, with some caveats. Turns out that designing things in a controlled area makes it hard to account for adverse affects from new environments. In particular, the practice rooms at AGDQ were filled with active CRTs, and they introduced substantial electromagnetic interference on the data lines. After some emergency troubleshooting and quickfixes, it was stable enough and worked through the run.

<div class="auto-resizable-iframe"><div style="text-align:left;"><iframe width="854" height="480" src="https://www.youtube.com/embed/NVHTd8faivI?start=1595" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div></div>