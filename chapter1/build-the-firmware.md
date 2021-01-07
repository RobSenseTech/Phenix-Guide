# Build the Firmware

Here is a simple process for developers to compile the source code.

## PhenixPro Devkit

Below shows how to build ArduCopter for the PhenixPro Devkit V2.0

First,Enter the specified directory:

```text
cd TrackingDemo_DevkitPro_linux
```

The next command should be called only once or when you want to change a configuration option. One configuration often used is the --board option to switch from one board to another one. For PhenixPro Devkit V2.0 we could switch to rst\_zynq and build:

```text
./waf configure --board rst_zynq
```

Last,Compile all:

```text
./waf copter
```

And if you want to know how to build linux and uboot, see the directory blow:

Basis of SW/HW co-design with DevKit/Get Started/Build Software

