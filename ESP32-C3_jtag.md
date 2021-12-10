---
title: JTAG Flashing
parent: ESP32-C3
has_children: true
nav_order: 1
---

# JTAG Flashing

In this document the ESP32-C3-DevkitM-1 and the ESP-PROG programmer are used. Vscode is running on Windows 11.

## Connection

|ESP32-C3-Mini-1 (PIN)| ESP-PROG   |
|:-------------------:|:----------:|
|VCC (2)              |VCC (1)     |
|GPIO4 (11)           |ESP_TMS (2) | 
|GPIO6 (9)            |ESP_CLK (4) |
|GPIO7 (8)            |ESP_TDO (6) |
|GPIO5 (10)           |ESP_TDI (8) |
|GND (1)              |GND (9)     |

