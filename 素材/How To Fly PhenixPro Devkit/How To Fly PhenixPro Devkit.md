# How To Fly PhenixPro Devkit

[TOC]

## 1.Download Source Code

Download code from github:

```
git clone https://github.com/RobSenseTech/PhenixPro_Devkit
```

compile code under the guidance of [prj_path]/README.md

**Note**: From now on, we have two branch on github:

- master
- develop

master is the release branch, we only modify code on develop branch, and merge it to master after new code have been tested well.

## 2.Boot

Devkit support boot from sd card, copy these file to sd card:

```
1.[prj_path]/BOOT.BIN
2.[prj_path]/amp_system/linux_image/devicetree.dtb
3.[prj_path]/amp_system/linux_image/uImage
4.[prj_path]/amp_system/linux_image/uramdisk.image.gz
```

set DIP switch like the image below(it means boot from sd card):

![webwxgetmsgimg](webwxgetmsgimg.jpg)

## 3.Connect UAV Components

![devkit](devkit.jpg)

As red words in image above, we can connect UAV component like this:

- Remote control receiver connect to **SBUS** (pin order from top to bottom is signal, vcc, GND)
- Four motors connected to **MOTO 1 to 4**, respectively (pin order from top to bottom is signal, vcc, GND)
- Ground station can be connected through **SERIAL** **4** port  on the board with baudrate 115200, while through other **SERIAL** ports with baudrate 57600.
- Connect power distribution board to **POWER**
- UAV head direction is the same as x axis which is marked in red box

