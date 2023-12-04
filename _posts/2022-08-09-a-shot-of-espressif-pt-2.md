---
layout: post
parent: Posts
title: "A Second Shot of Espressif: Flashing an Espressif ESP01s with an arduino"
author: "Sean Webster"
categories: [blog, projects]
tags: [espressif, ESP8266, ESP01, arduino, tutorial]
image: bee_flower.jpg
toc: true
---
<sup>Picture: Bumble bee and Anise Hyssop</sup>

*Realistically*, I should be following proper ESD precautions (ESD mat, grounding bracelet, etc (It's worse than 
you think, the ESD is about 2 feet to the right on where I'm working, and covered in my work stuff))

So, I've built the circuit. Time to test it. There are multiple ways to do this, ranging from super easy to
something akin to tossing it over the wall and hoping you pressed the right button. 

# Working Methods
## Flashing ESP-01s with Arduino IDE: The easiest
ESP8266 Arduino Core has [instructions](https://arduino-esp8266.readthedocs.io/en/latest/installing.html) to download 
the ESP8266 board profile. Do that.

Select the board (Generic ESP8266 Module)

![Generic ESP8266 Module](/../assets/img/arduino_ide_board_select.PNG)

Set the port (which has your arduino device (COM4 for me))

![Arduino port](/../assets/img/arduino_ide_port.PNG)

Set the Builtin LED to 2

![Builtin LED](/../assets/img/arduino_ide_led.PNG)

Load up blinky

![Blinky](/../assets/img/blink.PNG)

Press compile/upload. If there's trouble connecting to the ESP01, press that button that's connected to reset the ESP01 into
bootloader mode. A blue LED should flash if it's hooked up properly.

Once it's finished flashing, unplug the USB, and un-ground GP0 on the ESP01s plug the USB back into provide power, and our ESP01s
should be blinking on and off (success!).

## Building and flashing with mingw
### Setup Environment
This is all based on the [official Espressif getting started docs](https://docs.espressif.com/projects/esp8266-rtos-sdk/en/latest/get-started/windows-setup.html
)

Make sure you've got your [IDF](https://github.com/espressif/ESP8266_RTOS_SDK) cloned somewhere from the last post.

Also grab the [xtensa toolchain](https://dl.espressif.com/dl/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-win32.zip)

We will need the mingw32 terminal from [MSYS32](https://msys2.github.io/)

To make things easier, move the `examples\get-started\hello_world` folder to your project folder

in the MSYS32, run `mingw32.ext`. To get to your projects folder, `cd /<YOUR_DRIVE>/.../esp` (which shall now be referenced as `<YOUR_ESP>`)

Add the xtensa tool chain binary folder to your path `export PATH=$PATH:<YOUR_ESP>/xtensa-lx106-elf/bin`

Set your IDF_PATH `export $IDF_PATH=<YOUR_ESP>/ESP8266_RTOS_SDK`

### Building and Flashing
Now cd to your `hello_world` folder with `cd <YOUR_ESP>/hello_world`

do a `make menuconfig` and select `Serial flasher config`,
![menuconfig](/../assets/img/mingw_make_menuconfig.PNG)

then select `Default serial port` and hit enter.
![Default serial port](/../assets/img/mingw_make_menuconfig1.PNG)

If you know your port,
great, if you don't, you can check the arduino IDE, or you can check your system devices under COM ports.
![Enter serial Port](/../assets/img/mingw_make_menuconfig2.PNG)

Use the arrow keys to select the save option at the bottom and hit save. Then Exit.

Now, do a `make flash`. Theoretically, you should see a build happening.

After the build, comes the flash
![flash](/../assets/img/mingw_flash.PNG)

We can check our flash was a success with `make monitor`
![monitor](/../assets/img/mingw_monitor.PNG)

### Troubleshooting
If your ESP01s is not lighting up with the serial, try resetting it with. The LED lights up on every reset of the board.
the button in on the breadboard. If that isn't the issue, doublecheck your COM port

# Non-working Methods

## Flashing with CLion + PlatformIO - Broken
> [CLion with ESP-IDF](https://docs.platformio.org/en/latest/integration/ide/clion.html)
> 
>Starting with version 4.0, ESP-IDF uses a build system based on CMake. In order to provide more seamless integration, PlatformIO uses the CMake file-based API to extract build configurations. Because of this approach, there is a conflict between CMakeLists.txt used by ESP-IDF and CMakeLists.txt which PlatformIO generates for CLion. At the moment we’re working on better integration with CLion without this intermediate CMakeLists.txt, but there is no ETA for this feature.


~~Well, that's very disappointing... PlatformIO is a nice multiplatform tool, that abstracts away a bunch of the setup needed
for many microprocessors. However, that abstraction removes a lot of the freedom, and customization possible, especially 
with their generated cmake files.~~

See the post after this for details on getting this working 

[A Third Shot of Espressif: Flashing an Espressif ESP01s with an arduino using CLion and PlatformIO](2022-08-09-a-shot-of-espressif-pt-2.md)


## Building and flashing with CLion + Cmake - Broken
Cmake seems to be broken for the official ESP8266 SDK, which is a shame. (Or, at the very least, I can't get it working after
hours of troubleshooting) The submodules are causing many build issues.


## Flashing with Espressif Flash Tool
Open the IDF as a cmake project. Then open the blink project. (esp-idf/examples/get-started/blink/CMakeLists.txt)
The flash tool [can be found here](https://www.espressif.com/en/support/download/other-tools)
I may do a future writeup on this one, but not now.

# Further Reading
Here is some further reading, at least for me:

#### Open source sdk for ESP8266
https://github.com/pfalcon/esp-open-sdk

This seems worth checking out

#### ESP Tool
https://github.com/espressif/esptool

This is the tool for the ESP32, but it is included in the ESP8266 SDK?

#### ESP Modules
https://www.esp8266.com/wiki/doku.php?id=esp8266-module-family

This is the different ESP modules available

#### Example ESP8266 VS Project by Peteben
https://github.com/peteben/xPL-ESP8266
