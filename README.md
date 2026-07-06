# Mao Boy

A communist handheld gaming console based on the ESP-32 S3 capable of running multiplayer DOOM.
---

!['zine page](./Mao%20Boy.png)

## Features
- Peer-to-peer multiplayer
- Battery-powered handheld design
- Joystick w/ click controls
- 1.8" TFT display support (SPI-based)
- Low-latency ESP-NOW networkin

---

## Hardware

### Core
- Seeed Studio XIAO ESP32-S3

### Display
- 1.8" SPI

### Controls
- Joystick

### Power
- Standard 5V 10000mAh power bank

### 3D Printed Case
![top shell](./top_shell.png)
![bottom shell](./bottom_shell.png)

---

## Multiplayer System
[firmware source code](https://github.com/Eugene109/ESP32-DOOM)

This project uses ESP-NOW peer-to-peer communication**, allowing devices to connect directly without Wi-Fi infrastructure.

### How it works:
- Each device broadcasts player state packets
- Peers sync:
  - position
  - input states
  - game events
- No central server required
- Auto-discovery pairing mode supported
- Framebuffer optimized rendering pipeline
- Custom input handler
  

---


## Required Libraries
- ESP-IDF

## Flashing firmware
- Using ESP-IDF:
  - doom.py flash monitor
  - Or compile and upload using Arduino IDE.
 
Schematic:
![hello](./Schematic/Schematic.png)

With love,
Peter the eel
Made in Shenzhen China - 2026 Fallout HC
