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

## Pre Design
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

Are there any bits of the project I'm unfamiliar with?
* Powering without arduino
  
Have Seen Before But Not Great With?
* Wifi Security
* Onewire
* ESP8266 SDK
* DS18B20
  
What parts of the project are still a black box?
* Power
* Enclosure

## Design
### Hardware Components
- ESP01
- [DS18B20](https://www.analog.com/media/en/technical-documentation/data-sheets/DS18B20.pdf)
  
### Software Components
- [ESP8266 RTOS SDK](https://github.com/espressif/ESP8266_RTOS_SDK/tree/master)
- DS18B20 Driver


## Prototyping








## Productizing
https://github.com/StanislavLakhtin/esp-idf-onewire/tree/master
https://github.com/Tom-TheBrand/esp32_onewire
https://github.com/PaulStoffregen/OneWire
https://github.com/DavidAntliff/esp32-ds18b20
https://github.com/DavidAntliff/esp32-owb
