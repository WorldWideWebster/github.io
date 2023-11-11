---
layout: post
title: "Espressif Fair Trade Bean Edition: Inspecting the esp-open-sdk and esp-open-rtos"
author: "Sean Webster"
categories: blog, projects
tags: [blog, espressif, ESP8266, ESP01]
image: frog_wall.png
toc: true
---

They say that the average cup of espresso is half the caffeine of a full cup of coffee (They being a misremembered google search.
It turns out that sources are all widely speculative, and can't even agree on the average volume of a regular coffee or espresso shot). 
We can only hope that a shot of espressif has no corellation to java


# Exploring the ESP-OPEN-SDK
So, there exists an open source version of the esp8266 idf, using freertos, created by pfalcon. Cool.

[https://github.com/pfalcon/esp-open-sdk](https://github.com/pfalcon/esp-open-sdk)

Digging in, it seems pfalcon has largely abandoned the project, but multiple efforts exist to revive it.


## There exists some forks that work
This one [https://github.com/ChrisMacGregor/esp-open-sdk](https://github.com/ChrisMacGregor/esp-open-sdk)

And this one, thought it is set up weird [https://github.com/esp-open-sdk/esp-open-sdk](https://github.com/esp-open-sdk/esp-open-sdk)

*** Note: There exists a way to build this on Windows, however that requires some crosstool/automake configurations that I haven't the time for ***

### Honorable Mentions
A docker container [https://hub.docker.com/r/larsks/esp-open-sdk](https://hub.docker.com/r/larsks/esp-open-sdk)

A promising fork, that builds a

## This is a shame
Mostly because I wanted to try out the examples at [https://github.com/SuperHouse/esp-open-rtos](https://github.com/SuperHouse/esp-open-rtos)
fter updating the crosstool submodule [https://github.com/someburner/esp-open-sdk](https://github.com/someburner/esp-open-sdk)