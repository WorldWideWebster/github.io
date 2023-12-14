---
layout: tutorial
parent: Tutorials
title: "Using a Custom Library In KiCad in Windows"
author: "Sean Webster"
categories: tutorial
tags: [Tutorials,KiCad,arduino,tutorial]

---


Having Learned of KiCad recently, and with my alma matter killing student emails for alumni, I felt it was time to move away from EagleCAD.
The KiCAD UI is intimidating, opening it up for the first time.

I couldn't find these instructions quickly enough, so hopefully search engine web scraping is powerful enough to save other 
people 40 or so minutes it took me to figure this out.

These instructions may work for linux
# Using a Custom Library
KiCad by default saves user files to `C:\Users\[your name]\Documents\KiCad\6.0, or similar`
I've Created a folder libraries in said directory, and put my libraries in it,
I'm using [jdunmire's ESP8266 library](https://github.com/jdunmire/kicad-ESP8266)



Select the preferences in the top bar

![Preferences](/../assets/img/KiCad/1.JPG)

Select Manage Symbol Libraries

![Manage Symbol Libraries](/../assets/img/KiCad/2.JPG)

Then Global Libraries tab

![Global Libraries](/../assets/img/KiCad/3.JPG)


Then the Folder Icon(Add existing library from file)


![Folder Icon(Add existing library from file)](/../assets/img/KiCad/4.JPG)

Then locate the .lib file for the library you want to add and click ok

![your library file](/../assets/img/KiCad/5.JPG)

Hopefully, Sucess!

![Success!](/../assets/img/KiCad/6.JPG)


Very Cool

![Very Cool](/../assets/img/KiCad/7.JPG)


Now... back to actually trying to get work done on projects...