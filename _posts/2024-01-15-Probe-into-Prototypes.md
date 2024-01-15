---
layout: post
parent: Posts
title: "Probe into Prototypes: The IoT Temp Probe Project Update"
author: "Sean Webster"
categories: [blog, projects]
tags: [blog]
image: pantheon.jpg
toc: true
---
<sup>Picture: Ceiling of Pantheon, Rome, Italy September 2023</sup>

In this post, I'm diving into some recent developments in my IoT project and sharing my latest reads that have offered me some thought-provoking perspectives on technology and its future. You can thank ChatGPT for the title, I had nothing.


# Project Update: IoT Temp Probe
I've made much more progress on the IoT Temp Probe. I've nearly finished the hardware development, and have started working on the final software.

{% assign prototyping = site.pages | where:"url", "/Projects/iot_temp_probe/prototyping/" | first %}

{{ prototyping.content }}
This content can  be found at [the IoT Temp Probe Design Overview page](/Projects/iot_temp_probe/prototyping/)


# What I'm reading, watching, and listening to
## The Grid: The Fraying Wires Between Americans and Our Energy Future
I first heard of The Grid in a mention by [The Amp Hour](https://theamphour.com/) podcast. It is a peek behind the scenes at the US electrical infrastructure. It gives an in depth look at the history of the policy and technologies that made the US electrical grid what it is today. Overall, it was an interesting read, and gave nuanced insight into various statements I've heard from my Town's Power Co-op director on the subject of power generation capacity. 
The key takeaways from it where that

1. Peak Demand often does not line up with peak generation (due to renewables)
2. There needs to be something to handle the base load when generation stumbles
3. As is, the US grid is not a stable system

These were not new revelations to anyone semi familiar with the matter, but still a good read.

It can be found on Amazon, [here](https://www.amazon.com/Grid-Fraying-Between-Americans-Energy-ebook/dp/B01DM9Q6CQ)

## Backlog of Embedded Online Conference
I've signed up to attend the [Embedded Online Conference](https://embeddedonlineconference.com/) this year. They make all previous talks available, so I've been perusing them. The [Video Speed Controller](https://chromewebstore.google.com/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk?pli=1) chrome plugin makes this much easier. So far, after watching about 5 talks, nothing is completely ground breaking, but the quality isn't bad, either. The most interesting one I've seen so far is about OOP in C.

# Rabbit Holes
[What are coreless DC motors?
](https://www.motioncontroltips.com/what-are-coreless-dc-motors/) came up in the Embedded.fm slack channel, and I had never heard of 'coreless dc motors'

[Scroll Compressor Exposed: Understanding Its Mechanical Magic
](https://www.youtube.com/watch?v=e_4ITFCQvts) was suggested by the YouTube algorithm, and it was a good watch. As someone looking to replace their HVAC, it was interesting subject matter.

Hopefully, by next post, I should have the hardware in hand, and a large portion (if not all) of the IoT Temp Probe finished.