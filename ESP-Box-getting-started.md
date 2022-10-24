---
title: Getting-Started 
parent: ESP-Box 
grand_parent: ESP32-S3
nav_order: 1
---

# Getting started
In this document we'll see how to flash your first program in the ESP32-S3-Box, the example ```image_display```.

## Prerequisites
To start compiling and flashing you need to have installed:
* ESP-IDF (here the v4.4 will be used) - better if installed through vscode plugin
* Vscode (not mandatory but highly recommended)

## Cloning and building the project

The first step open a terminal and hit
```git clone --recursive https://github.com/espressif/esp-box.git ```

It wil take some time. The folder esp-box is created with all the required components and exaples.

Without entering the folder, copy the exaple in your current directory:
```cp -R esp-box/examples/image_display . ```
and then copy the components folder in the newly created ```image_display``` directory
```cp -R esp-box/components image_display```

Now you move to the ```image_display``` directory and open vscode ``` code . ```.

## Compiling the project

At this point you can press ```ctrl+shift+p``` to open the vscode commmand line and start the build with ```ESP-IDF:Build your project```.

You may encounter a problem [TODO]
If this happens, open the configuration through the vscode command ```ESP-IDF: SDK Configuration Editor (menuconfig)``` and search for the word "bundle". You need to uncheck the box and build the project again.

At this point you shouldn't get any error. Now you can flash the project with vscode command ```ESP-IDF:Flash your project```.

## Result








