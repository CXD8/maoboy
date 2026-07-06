# ESP32-S3 XIAO Handheld Doom (Peer-to-Peer Multiplayer)

Game Boy–style handheld gaming device built on the Seeed Studio XIAO ESP32-S3 running a lightweight port of [ESP32-DOOM, a port of PrBoom to the ESP32
]([https://google.com](https://github.com/espressif/esp32-doom)) with **peer-to-peer multiplayer over ESP-NOW**.


---

## Features

- Peer-to-peer multiplayer
- Battery-powered handheld design
- Joystick w/ click controls
- 1.8" TFT display support (SPI-based)
- Low-latency ESP-NOW networking

---

## Hardware

### Core
- Seeed Studio XIAO ESP32-S3

### Display
- 1.8" SPI

### Controls
- Joystick with click


### Power
- 3.7V LiPo battery
- TP4056 charging module (or built-in charging board)
- Power switch

---

## Multiplayer System

This project uses ESP-NOW peer-to-peer communication**, allowing devices to connect directly without Wi-Fi infrastructure.

### How it works:
- Each device broadcasts player state packets
- Peers sync:
  - position
  - input states
  - game events
- No central server required
- Auto-discovery pairing mode supported

---

## Software Stack

- ESP-IDF / Arduino framework (ESP32-S3)
- ESP-NOW networking layer
- Framebuffer optimized rendering pipeline
- Custom input handler

---


## Required Libraries
- #include <Arduino.h>
- #include <WiFi.h>
- #include <esp_now.h>
- #include <esp_wifi.h>
- #include <SPI.h>
- #include <Adafruit_GFX.h>
- #include <Adafruit_ST7735.h> 

## Flashing firmware
- Using ESP-IDF:
  - doom.py flash monitor
  - Or compile and upload using Arduino IDE.
