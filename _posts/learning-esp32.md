---
layout: post
title: "Learning the ESP32"
author: "Sean Webster"
categories: blog
tags: [blog]
image: nimbus_birthday.jpg
clionID: M6fa7tzZdLw
---

**Getting back into the flow of things...**

I swear, I'm not actively finding other things to do that aren't my programming projects... That's not quite true...
I've planted out a vegetable garden, increased my blueberry patch, cut down and mulched some trees, started on my micro table grape vinyard, 
and put a second deep box on my beehive since the last post.
## ESP-IDF plugin install for clion

>ESP-IDF is the development framework for Espressif SoCs supported on Windows, Linux and macOS.

My favorite IDE is currently CLion, and if I didn't get an account through work for free, I'd possibly buy it
(the single developer license is ~$100 a year last I checked). However, VSCode is quickly catching up, so who can say
what will be my favorite IDE next year.

Any ways, I digress. Jetbrains has made a nice video for integrating

{% include youtubePlayer.html id=page.clionID %}

The IDF can be found [here](https://github.com/espressif/esp-idf) 

## First some hardware setup...
So... a few years ago, I ordered some ESP-01ses. They sat around for a bit. Then a few years later I ordered some 
adapter boards. I had started to create a similar, more complex project, with larger scope, and more planning. 
I don't remember why I dropped it, but I plan for this project to be a modular rebirth of that project.

The [ESP01s](https://www.microchip.ua/wireless/esp01.pdf) is an 8-pin board with an ESP8266 on it, and oh boy are they cheap 
(can be had for as little as $2.39, even in the shortage!). It's got 2.4 GHz wifi, SDIO 2.0, (H) SPI, UART, I2C, I2S, IRDA, PWM, etc.
It's a 32-bit chip on the board, so it is more than ample for my needs. 

### Flashing the ESP-01s
The ESP-01s is only 8 pins, but it is easily flashable with an arduino uno (or similar), a USB cable, and some jumpers.

I've also found some esp32 examples that [masoncj created](https://github.com/masoncj/esp32-examples)



## Ki-CAD

