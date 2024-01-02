---
layout: page
title: Prototyping
parent: IoT Temperature Probe
grand_parent: Projects
nav_order: 3
---
# Draft
## Hardware Prototyping

### Assembling the circuit
Now that the initial design is out of the way, I can finally start assembling the circuit (This may have been completed before the start of the writeup). There are a few ways to adapt the ESP01 to work with a breadboard, and I chose an [adapter board](https://www.amazon.com/Stemedu-Breakout-Breadboard-Pre-Solder-Transceiver/dp/B07KBZRZ3Y), but not this specific one, from amazon.

To interface the DS18B20 with the breadboard, I solder some pins on the leads. I'm also missing a switch for the GPIO0 boot pin, so right now I'm attaching and removing a jumper.

![Picture of assembled circuit](/assets/img/temp_probe/breadboard.jpg)
### Testing the circuit
### General Test
As is tradition, I loaded it with reliable ol' Blinky.

By following [my own tutorial to flash with an arduino](/Tutorials/ESP01-arduino-flash/), I can easily load up software to test that everything is connected. I'm using [Simon Peter's ESP8266 Blink](https://gist.github.com/buildcircuit/bea2f7d606638dd73b1f)

![Blinky running](/assets/img/temp_probe/blinky.gif)

### DS18B20 Test
Doing similar, I load up the [DS18B20 Arduino example](https://github.com/jmchiappa/DallasTemperature/blob/master/examples/Simple/Simple.pde)

The output shows it is working
![DS18B20 Output](/assets/img/temp_probe/DS18B20_arduino.PNG)

### WiFi Test
Using the [Arduino ESP8266 WifiClient Example](https://github.com/esp8266/Arduino/blob/master/libraries/ESP8266WiFi/examples/WiFiClient/WiFiClient.ino),
Wifi is easily tested.

![Wifi test output](/assets/img/temp_probe/wifi_arduino.PNG)


### MQTT Test
#### Homeassistant MQTT Configure
To get Homeassistant to view any mqtt topics:
1. Go to settings->Integration entries->mqtt->configure
2. Listen to '#'
3. Find topic 'homeassistant/x/y'
4. Subscribe to topic
5. Set up payload like so https://www.home-assistant.io/integrations/mqtt#sensors
   1. Configure [discovery](https://www.home-assistant.io/integrations/mqtt#discovery-topic)
6. Configure your configuration.yaml file [like so](https://www.home-assistant.io/integrations/sensor.mqtt/)

I've used the Adafruit [MQTT_ESP8266 example](https://github.com/adafruit/Adafruit_MQTT_Library/blob/master/examples/mqtt_esp8266/mqtt_esp8266.ino)

Here is my Home Assistant MQTT server receiving the MQTT messages
![HASS MQTT](/assets/img/temp_probe/hass_arduino_mqtt.PNG)

## Software Prototyping
Throwing all of the code from the Arduino examples looks like this:
<h3><details closed>
    <summary>Github Gist</summary> 
    <script src="https://gist.github.com/WorldWideWebster/bce192e94e35830e9c5bd0e2dc667ba6.js">  </script>
</details>
</h3>

### Server Side
Here is my Home Assistant MQTT server receiving the new formatted MQTT messages
![HASS MQTT final](/assets/img/temp_probe/hass_arduino_mqtt_final.PNG)

And here it is displayed in the dashboard
![HASS MQTT dashboard](/assets/img/temp_probe/hass_arduino_display.PNG)

## Next Steps
With the prototype proving everything in theory works, it's time to solidify the design. Next comes the board design.
After that, the software implementation.