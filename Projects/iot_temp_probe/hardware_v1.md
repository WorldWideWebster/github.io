---
layout: page
title: Hardware V1
parent: IoT Temperature Probe
grand_parent: Projects
nav_order: 4
---

## Hardware Developement
### ESP-PROG
I was looking into a JTAG-esque header for this project, and was reminded of the 
[ESP-PROG board](https://docs.espressif.com/projects/espressif-esp-iot-solution/en/latest/hw-reference/ESP-Prog_guide.html) by Espressif. It is available [from Mouser](https://www.mouser.com/ProductDetail/Espressif-Systems/ESP-PROG?qs=0lSvoLzn4L9lCAjJ8r9cdg%3D%3D)

I was unaware it worked for the ESP8266, but after ordering one, I have confirmed that it does. I then put a ESP-PROG header on my board.
![ESP-PROG setup](/assets/img/temp_probe/hardware/esp-prog.jpg)

To flash from WSL Ubuntu, I used the command:
`idf.py flash -p /dev/ttyS9 -b 115200`

### Layout
Using KiCad, I've drawn up a board for my temp probe. I followed [this tutorial](https://www.youtube.com/watch?v=aVUqaB0IMh4) for layout. I also had a bunch of help from some friends and a few people from the Embedded.fm Slack channel.

![board layout in kicad](/assets/img/temp_probe/hardware/layout.PNG)

Top Render in KiCad:
![top render in KiCad](/assets/img/temp_probe/hardware/iot_temp_probe_top.PNG)

Bottom Render in KiCad:
![bottom render in KiCad](/assets/img/temp_probe/hardware/iot_temp_probe_bottom.PNG)

I found a useful collection of [open source KiCad Libraries](https://github.com/benwis/SparkFun-Kicad-Libraries/tree/master)

I decided to go with a [JST XHP-3 Connector](https://www.digikey.com/en/products/detail/jst-sales-america-inc/XHP-3/1651017) for the DS18B20.

### Manufacturing
[JLPCP](https://jlcpcb.com/capabilities/pcb-capabilities) is what I used, which was recommended in the youtube video.

There are useful tools to generate BOM files for JLCB, such as [this plugin](https://github.com/wokwi/kicad-jlcpcb-bom-plugin)

There is also another interesting [BOM generator](https://github.com/SchrodingersGat/KiBoM) I did not have time to test.

I sent the design out, only to find out that the footprint for my LM3671 was wrong. I had used a SOT5x3 vs SOT23
Luckily, they caught my error, and I was able to cancel the order with populated components.

I did, however, keep my order of unpopulated PCBs. It was cheap enough, and it was a good silkscreen test.
I ended up adding some pictures of my dog, because why not.

The silkscreen came out pretty good
![V1 Rev A board](/assets/img/temp_probe/hardware/v1_revA.jpg)

Here is a grayscale render. I've been looking into a way to render more than stls.

{% include stlviewer.html src="boardv1.stl" width=500 height=300 extrastyle="" %}

I've sent out a fixed version of my files to JLPCB, and am awaiting populated boards.

### Next Steps
Hopefully my fixed rev B of the board arrives, and I can load software on it. The production version of software is still in progress, so I plan to continue work on that.

### Future Plans
I plan to cover the vinyl portion of the DS18B20 with [food grade tubing](https://www.amazon.com/Temperature-Shrink-Silicone-Rubber-Tubing/dp/B06W51VZ43)