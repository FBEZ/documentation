---
title: JTAG Flashing ESP32
parent: ESP32
has_children: true
nav_order: 1
---

# JTAG Flashing

In this document the ESP32-Devkit-C and the ESP-PROG programmer are used. Espressif-IDF is running on Windows 11.

## Install Espressif-IDE

Download the installer [here](https://github.com/espressif/idf-installer#espressif-ide-offline-installer) and follow the installation procedure.

### Test the installation
Start a new project as explained [here](https://github.com/espressif/idf-eclipse-plugin/blob/master/README.md#create-a-new-project) and check that you can compile and flash through the USB port. 

## Connection JTAG
Connect the ESP-PROG and ESP32-WROOM-32E pins as show in the table below. The table lists the pin name and the pin number in brackets.

| ESP32-C3-Mini-1 (PIN) | ESP-PROG (PIN) |
|:---------------------:|:--------------:|
| VCC (2)               | VCC (1)        |
| MTMS / GPIO14         | ESP_TMS (2)    |
| MTCK / GPIO13         | ESP_CLK (4)    |
| MTDO / GPIO15         | ESP_TDO (6)    |
| MTDI / GPIO12         | ESP_TDI (8)    |
| GND (1)               | GND (9)        |

[Reference](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/jtag-debugging/configure-other-jtag.html) 


## Project setup

Follow the steps [here](https://www.beyondlogic.org/debugging-with-jtag/) from the section " Debugging Configurations in EclipseDebugging Configurations in Eclipse" to setup the commands. In "run->debug configuration" setup the esp-prog:

![e77078da6704828ae92729921dbd42ac.png](images\esp32_jtag\e77078da6704828ae92729921dbd42ac.png)


If you're using the hello_world example, add to the startup tab the line
```
mon program_esp ${workspace_loc:hello_world/build/hello_world.bin} 0x10000 verify
```

Now hit debug.. If you get ```Error: libusb_open() failed with LIBUSB_ERROR_NOT_FOUND``` follow the procedure [here](https://community.platformio.org/t/esp32-pio-unified-debugger/4541/20) to replace the drivers.

Now the debugger will start and work.


