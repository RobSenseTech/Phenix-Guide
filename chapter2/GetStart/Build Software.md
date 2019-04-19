# 2. Build Software

## 2.1 For PhenixPro Devkit

This section will show you a simple way to build software for PhenixPro Devkit V2.0

### 2.1.0 u-boot

Get u-boot source code from github:

```
git clone https://github.com/RobSenseTech/PhenixPro_Devkit_V2.0
cd PhenixPro_Devkit_V2.0/uboot-xlnx
```

Make the configuration effective:

```
make phenixpro_devkit_config
```

Complie u-booot:

```
make ARCH=arm CROSS_COMPILE=arm-xilinx-linux-gnueabi- -j8
```

Last step, rename u-boot to u-boot.elf.And you can use it to create BOOT.bin by SDK.

Note: compile error handle:

fatal error: openssl/evp.h install openssl:

```
sudo apt-get install libssl-dev
```

./bin/sh: 1: dtc: not found install dtc:

```
sudo apt-get install device-tree-compiler
```

### 2.1.1 Linux Kernel

Enter the linux kernel directory:

```
cd PhenixPro_Devkit_V2.0/linux-xlnx-4.9
```

Compile kernel:

```
cp arch/arm/boot/phenixpro-devkit-config/devkit-config .config

make ARCH=arm CROSS_COMPILE=arm-xilinx-linux-gnueabi- menuconfig
Device Drivers  --->
        [*]Pulse-Width Modulation (PWM) Support  --->
        <*>   Xilinx PWM support

make ARCH=arm UIMAGE_LOADADDR=0x8000 CROSS_COMPILE=arm-xilinx-linux-gnueabi- uImage -j8
```

### 2.1.2 Linux Devicetree

Generate dtb file with command

```
cd PhenixPro_Devkit_V2.0/linux-xlnx-4.9
./mkdtb.sh
```

### 2.1.3 Linux Filesystem

Get Linux Filesystem from github:

```
https://github.com/RobSenseTech/PhenixPro_Devkit_Platform
```

generate Linux Filesystem with command

```
cd PhenixPro_Devkit_Platform/filesystem/ramdisk/
./mkramfs.sh rootfs
```



question 1: how to run your own application in Phenix Pro board.

if you want to run your own application,before you make Linux Filesystem,you must put you executable file in /usr/, our arducopter executable file also at here.



question 2:how to bind your own application to a specific CPU core.

our arducopter application was bound to run in a specific CPU core,if you want to do the same,reference document:/etc/init.d/rcS.

A command named "taskset" can achieve your goal.



