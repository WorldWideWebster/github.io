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




# Design
## Hardware Components
- ESP01
- [DS18B20](https://www.analog.com/media/en/technical-documentation/data-sheets/DS18B20.pdf)
- Power Supply (Currently Unknown)
  
## Software Components
- [ESP8266 RTOS SDK](https://github.com/espressif/ESP8266_RTOS_SDK/tree/master)
- DS18B20 Driver
- Wifi
- [ESP CoreMQTT](https://github.com/espressif/esp-freertos-coremqtt)


# Prototyping

Plenty of tools exist for software prototyping. I've chosen to use arduino

## Power Supply
The ESP8266 Draws 300mA max, during Wifi transmissions, according to multiple sources on the internet. The data sheet says 170 mA max. I'll err on the side of caution
The DS18B20 draws 4mA, which is negligible.

The [Adafruit LM3671 3.3V Buck Converter Breakout](https://www.adafruit.com/product/2745) fits my needs well.









## Productizing
https://github.com/StanislavLakhtin/esp-idf-onewire/tree/master
https://github.com/Tom-TheBrand/esp32_onewire
https://github.com/PaulStoffregen/OneWire
https://github.com/DavidAntliff/esp32-ds18b20
https://github.com/DavidAntliff/esp32-owb
