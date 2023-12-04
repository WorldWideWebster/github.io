---
layout: post
parent: Posts
title: "Wifi Thermometer"
author: "Sean Webster"
categories: [blog, projects]
tags: [blog]
image: rome1.jpg
toc: true
---

# Wifi Thermometer
The hardest part, to me, about project design, is starting it. The second hardest part is figuring out how to do the rest of it.

I find a well done project starts with a good plan. A good plan is one that is simple, yet adaptable. The easiest way to plan is to know the problem trying to be solved.

So, what is the goal here?
>To measure temperature, and send that data back over wifi

What are my constraints?
* hardware - I want to use hardware I already have, namely esp8266 and ds18b20
* languages - I want to use C++
* I'm lazy - I want to find open source libraries that do the things I want

Now that I know my constraints, are there any conflicts?
> No, all of these things work together.

Ok, then are there any foreseeable problems?
* How will this get powered?
* Licensing?
* Weatherproof?