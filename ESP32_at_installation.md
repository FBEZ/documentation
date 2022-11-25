---
title: Installing AT firmware
parent: ESP32
has_children: true
nav_order: 1
---

# Installing AT firmware

To install the AT firmware, we will use the `esptool`.

## Installing esptool

Open a terminal as administrator. 
```
python.exe -m pip install --upgrade pip
pip install esptool
```
Check if the installation worked properly with `esptool.py -h`. 
You can check the connection with an ESP board by using the command `esptool.py read_mac`
```bash
esptool.py v4.4
Found 1 serial ports
Serial port COM8
Connecting....
Detecting chip type... Unsupported detection protocol, switching and trying again...
Connecting..........
Detecting chip type... ESP32
Chip is ESP32-D0WD (revision v1.0)
Features: WiFi, BT, Dual Core, 240MHz, VRef calibration in efuse, Coding Scheme None
Crystal is 40MHz
MAC: 40:f5:20:71:d7:20
Uploading stub...
Running stub...
Stub running...
MAC: 40:f5:20:71:d7:20
Hard resetting via RTS pin...

```


