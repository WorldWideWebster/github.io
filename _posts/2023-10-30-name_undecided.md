---
layout: post
title: "And Now for Something Completely Different"
author: "Sean Webster"
categories: blog, projects
tags: [blog, espressif, ESP8266, ESP01, arduino, tutorial, blinky, PlatformIO]
image: frog_wall.png
toc: true
---

Over a year has passed since my last post. 

Time for a new project. For legal reasons, I can't touch my last idea for a year.

A new idea for a project: An indoor irrigation system.
The plan:

```plantuml
@startuml
title System Diagram for Indoor Irrigation
component MCU
component "Motor Driver"
component Radio
component pump
component "Conductivity Sensor"
cloud "Home Server"

MCU  -> "Motor Driver"   : pwm
"Motor Driver" -> MCU   : voltage
MCU -> Radio            : i2c
Radio -> MCU            : i2c
"Motor Driver" -> pump
Radio -> "Home Server"
"Conductivity Sensor" -> MCU
@enduml
```

It's simple enough, and fits with my needs and wants.

```plantuml
@startuml
newpage

node test
node tes1

test -> test1
@enduml
```


https://github.com/simplefoc/SimpleFOCMini
https://docs.simplefoc.com/

https://feilipu.me/2011/09/22/freertos-and-libraries-for-avr-atmega/
https://github.com/feilipu/avrfreertos
