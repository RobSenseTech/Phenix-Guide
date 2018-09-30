Here is a simple process for developers to compile the source code.

## PhenixPro Devkit V1.0
compile cpu1 BSP(Board Support Package):

```
make bsp-clean;make bsp -j8
```

compile pilot code:

```
make pilot-clean;make pilot -j8
```

compile all:
```
make clean;make -j8
```
**Note:**
​	Bcause the pilot code depends on cpu1 bsp, please make sure that you have compiled bsp before compiling pilot code.



## PhenixPro Devkit V2.0
Below shows how to build ArduCopter for the PhenixPro Devkit V2.0

First,Enter the specified directory:

```
cd TrackingDemo_DevkitPro_linux
```

The next command should be called only once or when you want to change a configuration option. One configuration often used is the --board option to switch from one board to another one. For PhenixPro Devkit V2.0 we could switch to rst_zynq and build:

```
./waf configure --board rst_zynq
```

Last,Compile all:

```
./waf copter
```