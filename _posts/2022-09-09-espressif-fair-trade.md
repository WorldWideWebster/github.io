---
layout: post
parent: Posts
title: "Espressif Fair Trade Bean Edition: Inspecting esp-open-sdk and esp-open-rtos"
author: "Sean Webster"
categories: [blog]
tags: [blog, espressif, ESP8266, ESP01, FreeRTOS]
image: path1.jpg
toc: true
---
<sup>Picture: Jordan Pond Loop, Acadia National Park</sup>

They say that the average cup of espresso is half the caffeine of a full cup of coffee (They being a misremembered google search.
It turns out that sources are all widely speculative, and can't even agree on the average volume of a regular coffee or espresso shot). 
We can only hope that a shot of espressif has no corellation to java


# Exploring the ESP-OPEN-SDK
So, there exists an open source version of the esp8266 idf, using freertos, created by pfalcon. Cool.

Their own words:
>This repository provides the integration scripts to build a complete standalone SDK (with toolchain) for software development with the Espressif ESP8266 and ESP8266EX chips.
>
>The complete SDK consists of:
>
>1. Xtensa lx106 architecture toolchain (100% OpenSource), based on following projects:
>* https://github.com/jcmvbkbc/crosstool-NG
>* https://github.com/jcmvbkbc/gcc-xtensa
>* https://github.com/jcmvbkbc/newlib-xtensa
>* https://github.com/tommie/lx106-hal
>
>The source code above originates from work done directly by Tensilica Inc., Cadence Design Systems, Inc, and/or their contractors.
>
>2. ESP8266 IoT SDK from Espressif Systems. This component is only partially open source, (some libraries are provided as binary blobs).
>http://bbs.espressif.com/viewforum.php?f=46
>OpenSource components of the SDK are based on:
>
>* lwIP, http://savannah.nongnu.org/projects/lwip/
>* Contiki, http://www.contiki-os.org/
>* axTLS, http://axtls.sourceforge.net/
>* wpa_supplicant, http://w1.fi/wpa_supplicant/ (source withheld by Espressif)
>* net80211/ieee80211 (FreeBSD WiFi stack), http://www.unix.com/man-page/freebsd/9/NET80211 (source withheld by Espressif)

[https://github.com/pfalcon/esp-open-sdk](https://github.com/pfalcon/esp-open-sdk)

Digging in, it seems pfalcon has largely abandoned the project, but multiple efforts exist to revive it.


## There exists some forks that work
This one [https://github.com/ChrisMacGregor/esp-open-sdk](https://github.com/ChrisMacGregor/esp-open-sdk)

And this one, thought it is set up weird [https://github.com/esp-open-sdk/esp-open-sdk](https://github.com/esp-open-sdk/esp-open-sdk)

*** Note: There exists a way to build this on Windows, however that requires some crosstool/automake configurations that I haven't the time for ***

Following their build instructions on a clean ubuntu system makes a viable product, with only some minor headaches

### Honorable Mentions
A docker container [https://hub.docker.com/r/larsks/esp-open-sdk](https://hub.docker.com/r/larsks/esp-open-sdk)

A promising fork, that builds after updating the crosstool submodule [https://github.com/someburner/esp-open-sdk](https://github.com/someburner/esp-open-sdk)

# ESP-OPEN-RTOS [https://github.com/SuperHouse/esp-open-rtos](https://github.com/SuperHouse/esp-open-rtos)
In their own words:
> A community developed open source FreeRTOS-based framework for ESP8266 WiFi-enabled microcontrollers. Intended for use in both commercial and open source projects.
>
> Originally based on, but substantially different from, the Espressif IOT RTOS SDK.
 
I'll be honest, here, I came for the examples. They have a D18B20 example that I'm quite keen on. Building the esp-open-sdk
toolchain is required to use the esp-open-rtos, and with only some minor headaches is perfectly fine.

I can then load their blink and wifi examples, and then Robert is your father's brother.