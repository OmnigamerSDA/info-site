---
title: Chimera
subtitle: Universal Controller Remapper
layout: page
order: 2
icon: fa-gamepad
---

My experiences with Input Control and MashAttack left me with a pretty good understanding of interacting with controllers and consoles from microcontrollers. I started thinking about how I could apply these skills to something new and useful. My first thought was to start making input viewer hardware and software for all manner of other gaming controllers, but I decided that it would be a really inefficient and unrewarding process to just iterate through the different controllers and make minor adjustments for each. There had to be something better I could do.

<span class="image center"><img src="{{ 'assets/images/chimera.png' | relative_url }}" alt="" /></span>

That's where I started to consider the other implications of having full control of the communications between console and controller. In particular, I became interested in the idea of remapping controls to make for more comfortable inputs in specific situations. Some games have this feature built in, but many are limited in what they can do. Providing the ability to set up controls in whatever way lets you perform best seemed like a reasonable new set of functionality I could provide.

Then it occurred to me that I could take this concept a step further. Since I'm already putting a microcontroller in the middle, the controller and console don't necessarily have to match at all, so long as I can communicate with each in the proper way. Not only that, I could add in other special abilities, like authenticated logging, turbo, macros... 

Several months of design planning later, this concept would form the groundwork for what I'm tentatively calling Chimera. The idea is to have adapters for virtually any console and controller that enable players to take advantage of the full array of features, no matter what their console and controller of choice is. While I am still working on the design and implementation, I released an that discusses the main points of my approach and some of its major features. Look forward to more information soon!

<div class="auto-resizable-iframe"><div style="text-align:left;"><iframe width="854" height="480" src="https://www.youtube.com/embed/hdWulVCAS9w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div></div>