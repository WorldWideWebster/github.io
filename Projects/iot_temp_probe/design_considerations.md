---
layout: page
title: Design Considerations
parent: IoT Temperature Probe
grand_parent: Projects
nav_order: 1
---
## Design Considerations
Before I start writing the proof of concept software, it's a good idea to have a vague feeling of the direction I want the project to go.

### Project Goal and Scope
To measure temperature, and send that data back to a server via MQTT over Wifi.

### What are my constraints?
- **Hardware**: I want to use hardware I already have, namely ESP8266 and DS18B20.
- **Languages**: I want to use C and C++. These are my bread and butter languages, and learning new ones is not in the scope of this project.
- **I'm lazy**: I want to find open source libraries that do the things I want. I don't want to spend too much time reinventing the wheel.

### Are there potential conflicts?
No, all of these things work together.

### Foreseeable Problems?
- Power supply: How to efficiently get 3.3V to the device?
- Weatherproofing: Is making the device weatherproof necessary for this version?
- WiFi Security: This area is somewhat unfamiliar to me.
- Limited Hardware: Contingency plans if ESP8266 or DS18B20 supplies run low.
- OTA Updates: Understanding ESP8266 OTA functionality.

### Areas of Unfamiliarity
- Powering ESP8266 without Arduino.

### Familiar Areas but Not Expertise
- **OneWire**: Previously used with DS18B20 on Arduino. Familiar with the basics.
- **ESP8266 SDK**: Some experience in running examples, curious about its similarities with ESP32 IDF.
- **DS18B20**: Operational experience with Arduino libraries.
- **OTA Updates**: Experience with other systems, but not ESP8266.

### Black Box Areas
- **Power**: Understanding beyond the basic requirement of 3.3V input.
- **Enclosure**: Deciding between indoor or outdoor use.
- **WiFi Security**: Recognizing its importance but lacking deep knowledge.

### Confident Areas
- **FreeRTOS**: Extensive experience in a professional setting.
- **MQTT**: Frequently used in home automation projects.
- **Sensor Data Handling**: Both sending and receiving, in work and home contexts.