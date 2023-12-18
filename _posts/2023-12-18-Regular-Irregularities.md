---
layout: post
parent: Posts
title: "Regular Irregularities: A Move to Semi-Regular Blog Posts"
author: "Sean Webster"
categories: [blog, projects]
tags: [blog]
image: path2.jpg
toc: false
---
<sup>Picture: Jordan Pond Loop, Acadia National Park, ME</sup>

The hardest part, to me, about project design, is starting it. The second hardest part is figuring out how to do the rest of it.

I've had some parts laying around to build an IoT temperature probe, and I figure it's time I design and assemble this project.
The goal is to create an IoT Temperature Probe as a design to production product. The hope is to showcase some skills, and become more comfortable with the process. And to hopefully learn something.
Hopefully by fully documenting the process, it can work as a sort of tutorial or stepping stone for other people.
# Project Updates: IoT Temperature Probe
I'm officially introducing my IoT Temperature Probe project as in development.

{% assign tempProbe = site.pages | where:"url", "/Projects/iot_temp_probe/iot_temp_probe/" | first %}

{{ tempProbe.content }}

{% assign designConsiderations = site.pages | where:"url", "/Projects/iot_temp_probe/design_considerations/" | first %}

{{ designConsiderations.content }}

This can be found at [/Projects/iot_temp_probe/design_considerations/](/Projects/iot_temp_probe/design_considerations/)

# Blog Updates
## Site Improvements
I've made numerous updates to the blog. It's almost in a place where I can finally leave it and start doing the projects I want to share on the blog. I've moved to bi-weekly blog posts (as opposed to weekly updates), in an effort to keep updates regular, but to also give time to improve quality. For the time being, I want to commit to these semi-weekly blog posts, even if they're not of much substance, themselves. However, some of the pages and changes I've made are more work than a blog post. I would also like to move to a point where the blog is not the main focus of my time, as it seems to have eaten most of my project time.

I'm still in the mode of throwing everything at the wall to see what sticks, and to find the voice and audience of this blog. Right now, it's still just
a personal projects blog, with some (hopefully helpful) info sprinkled about. I plan to narrow the focus to electronics, but also keep my hobbies on the peripheral.

A recent blog update had caused it to greatly slow down. I've tried batch editing my photos to make them much smaller, and it seams to have worked.
Thanks to [BIMP](https://alessandrofrancesconi.it/projects/bimp/), a plugin for GIMP. It turns out I did not need to upload print quality photos to my blog.

I've found a quick workaround to embed project pages in blog posts thanks to [Kevin Workman on stackoverflow](https://stackoverflow.com/a/68092965/22897244) using Jekyll's liquid tags.

{% raw %}
```markdown
{% assign myOtherPost = site.pages | where:"url", "/Projects/iot_temp_probe/design_considerations/" | first %}

{{ myOtherPost.content }}  
```
{% endraw %}

## More Pages and Sections

I've added my [guitars projects](/Projects/Guitars), and specifically my work on my [Aria Pro II Knight Warrior](/Projects/Guitars/AriaProII_Knight_Warrior) that I recently completed,
and [My First Partscaster](/Projects/Guitars/first_custom_partscaster.md) that I did before then.

I've added the [ViewSTL Plugin](https://www.viewstl.com/plugin/), with a lot of help from [Slim Nate](https://slimnate.com/blogging/tutorial/2021/04/18/displaying-3d-models.html).
This allowed me to display my 3d models that I've created, [here](/Projects/3D_Printing/)

I've added the [Tutorials Section](/Tutorials/) and have condensed my previous tutorials and put them there.

I still have a bunch of completed and in progress projects that I plan to add to the projects pages.

# Misc
## A little retrospective
I've been reviewing old blog posts, specifically the post "Inspecting esp-open-sdk and esp-open-rtos". 
I've been looking at the [ESP8266 RTOS SDK](https://github.com/espressif/ESP8266_RTOS_SDK/tree/master), and honestly, I have no idea why I made the post. 
I think I may have had misconceptions of licensing for the idea I was thinking of productizing. Having worked professionally with the ESP32 IDF, that concern was a moot point. 
I now plan to work with the official SDK, which uses FreeRTOS, which removes a lot of the hassle of setup, due to the amount of people testing and contributing to it.

## What's on the workbench
Here's a peak to what I'm physically working on. I'm finding guitar maintenance and building to be a zen-like activity. I can throw on a podcast or audiobook, and just get to work.

![Samick Bass](/assets/img/guitars/samick_bass.jpg)
I recently picked up this bass as a thank you gift for a friend. This one was made in Korea, at the same factories that Fender had contracted to make their instruments in the 80's and 90's, post CBS acquisition.
I plan to give it a good cleanup and send it on its way. My workbench is a bit busy, and I'm still trying to figure out a happy medium for it, and this has caused the organization to be in a state of flux.

## Some interesting papers I've come across this week:
I've come across some interesting papers these weeks in discussions and research over/into hobbies.

* From a discussion of acoustic guitar bracing in a luthier facebook group:
[Frequency Response Evaluation of Guitar Bodies with Different Bracing Systems](https://www.mdpi.com/2073-8994/12/5/795)

* From a discussion with friends about automating knitting:
[A compiler for 3D machine knitting](https://dspace.mit.edu/handle/1721.1/134995)

* From a google search after a question about the curious death of some of my bees: 
[A New Threat to Honey Bees, the Parasitic Phorid Fly Apocephalus borealis](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3250467/)