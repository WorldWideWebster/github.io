---
layout: post
parent: Posts
title: "An Unscheduled Hiatus"
author: "Sean Webster"
categories: [blog, projects]
tags: [blog]
image: rome1.jpg
toc: true
---
<sup>Picture: Roman Street, September 2023</sup>

As I had embarked on my next employment opportunity in late winter 2024, I asked myself: 'what now?'. It was at this point that I remembered that when employed, free time is a precious thing. It's why remote work is so important to me - I get to save the hours of work a day, literal days of my life spent a year driving (I think it averages to about 10 days a year, assuming 1 hour spent commuting a day).  And here I come to my point. I had committed to weekly, then biweekly posts. And I think the only one that really matters to is me. So I've decided to only post when I have something I want to post. No more having ChatGPT fill in the blanks to push out a blog post for some arbitrary deadline I've set for myself.

The nice thing about keeping a blog? I get to forget what I was doing and still pick it back up later. Having picked up my IoT temp probe from earlier this year with more documentation than I get at most companies, I've realized the project was going in the wrong direction. As I've echoed in the previous statement, I'm starting to add more value to my time. After at least an hour of trying to get the ESP8266 FreeRTOS repo to build, I started to question why I was doing this. The pennies saved by using the ESP8266 and trying to get libraries to work, while the chip itself has been EOL'd seems to me now like a fools errand. I'm finding that I need to replace that chip.

I've found that pine64 has the [Pinenut Model-01S](https://pine64.com/product/pinenut-model01s-wifi-ble5-module/), which utilizes the BL602 from Boufalo Labs, which is a 1-1 drop in for the ESP-01S. This would allow me to keep the hardware the same. It has the added bonus of being a RISC-V processor. Would this be falling into the 'penny rich, dollar poor' trap I fell into in planning this project?

There is also the ESP32 C3 I've been hearing good things about.

Oh, hey, would you look at that: Past me has ordered PineNuts and a programmer when he ordered the PineCil. I guess I'll use that.

It can't be worse than what I was trying to do with the ESP01S... right?

Relatedly, it looks like I swapped some of the pins for the ESP01S module on my board, so I have to figure out a way to rectify that.

## What I've been up to
It's not like I've been idle in the mean time. Here's a summary:
* Replaced the stairs on my house
* Overhauled my irrigation system
* Did a ton of gardening, planted a bunch of fruit trees (apples, cherries, peaches, nectarines, pawpaws, persimmons, mulberries)
* Worked on a bunch of guitars and music.
* Geothermal for my house

There's a distinct lack of embedded work - that need was fulfilled by the contract I was on.

For the sprinkler system, I set a Raspberry Pi Zero up with [OpenSprinkler](https://opensprinkler.com) using
 [this tutorial](https://opensprinkler.com/forums/topic/tutorial-install-opensprinkler-unified-on-a-fresh-raspbian-image-for-a-pi-2/). I also thought it prudent to save [this link](https://opensprinkler.com/forums/topic/sprinklers_pi-an-alternative-sprinkler-control-program/) to another ui for the system, though I did not use it.

I've picked up a few podcasts, that I'd recommend
[Music Student 101](https://musicstudent101.com) - A podcast that's pretty much a university level music education
[You'll Hear It](https://youllhearit.com) - Daily jazz tips
[Strong Songs](https://strongsongspodcast.com) - Breaking apart famous songs to see what makes them different
[Musicality Podcast](https://www.musical-u.com/learn/welcome-musicality-podcast/) - Tips to become a better musician

## Next Steps
My next post will hopefully be soon, but I'm going to throw away an arbitrary schedule for a blog that is largely for myself. I'm going to migrate my IoT temp probe to the BL602 in the PineNut, and I'll see how that goes. I'll also fix the pins on my board.