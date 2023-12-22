---
layout: post
parent: Posts
title: "Irrigation"
author: "Sean Webster"
categories: [blog, projects]
tags: [blog]
image: rome1.jpg
toc: true
---
Time for a new project. For legal reasons, I can't touch my last idea for a year.

A new idea for a project: An indoor irrigation system.
The plan:


It's simple enough, and fits with my needs and wants.
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