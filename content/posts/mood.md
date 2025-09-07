---
title: "Building a Mood Barometer: The IoT Workshop at Swiss Re"
date: 2020-02-16
tags: ["iot", "workshop", "esp32", "mqtt", "azure", "hardware"]
---
## Building a Mood Barometer: The IoT Workshop at Swiss Re

n early 2020, I hosted a hands-on IoT workshop at Swiss Re. The challenge? Build a mood barometer — a physical dial that reflects the emotional "weather" of a space.

Each team flashed an ESP32, wrote Arduino code to read mood values over HTTP or MQTT, and moved a dial to match. No soldering — just ESP32 boards, stepper motors, and a magnet sensor wired up to detect calibration points. A few hundred francs in parts. Build it. Ship it. Make it move.

I prepped three micro-projects to help them get there:

- [**mood-barometer**](https://github.com/neilspink/mood-barometer):  
  ESP32-based analog mood dial powered by a stepper motor and magnet sensor. It listens for MQTT messages and moves the needle to happy, neutral, or sad. Includes the GIMP dial art and Fusion 360 housing.

- [**mood-infrared-controlled**](https://github.com/neilspink/mood-infrared-controlled):  
  For teams that didn’t want to mess with networking. Used any IR remote to manually set the mood. Just fun to play with.

- [**mood-mqtt-client-nodejs**](https://github.com/neilspink/mood-mqtt-client-nodejs):  
  Node.js MQTT publisher — a CLI tool to simulate inputs or act as a bridge between UI and device.

---

### ![Barometer prototype](/images/picture-front.jpg)
### ![Back of the Barometer](/images/picture-back.jpg)

---

A colleague stepped up and helped design a **custom PCB**, so teams weren't fumbling with jumper wires all day. That took things to another level. Everyone had something solid to build with — and take home.

Some used a **local MQTT bridge**, others connected to **Azure IoT Hub** with device provisioning and telemetry reporting. A few hundred francs in hardware, a shared repo, and some printed cheat sheets — that's all it took.

It turned out to be one of the most satisfying workshops I’ve ever run.