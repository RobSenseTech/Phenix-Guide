Here is a simple process for developers to compile the source code.

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
