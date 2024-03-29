---
layout: page
title: ESP32 Wireless Logger
description: Log messages over WiFi, using either TCP, UDP or Websockets
img: /assets/img/esp_wifi_logger_edited.gif
github: https://github.com/VedantParanjape/esp-wifi-logger
category: software
importance: 2
---

![](/assets/img/esp_wifi_logger_edited.gif)

* ESP32 is cheap microcontroller with WiFi, It runs a dual core processor clocked at 160Mhz.
* Created a component which sends log messages generated by the microcontroller over WiFi, using either TCP, UDP or Websockets, which is user selectable. It ensures a minimal memory footprint, 20kb when using UDP Sockets.

## Features

* Generates log messages with same format as ESP-IDF Logging API.
* Can route logs generated by ESP_LOGX(), provides a custom function to log messages over wifi.
* Follows ESP-IDF log color pattern for different log levels.
* Using UDP as network protocol provides lowest latency:
    * Minimal test condition - minimum free heap = 220388 bytes.
* TCP performance is mid-way:
    * Minimal test condition - minimum free heap = 216537 bytes.
* Using Websockets provides the worst latency:
    * Minimal test condition - minimum free heap = 205416 bytes.
