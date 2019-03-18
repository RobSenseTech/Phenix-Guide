# Get Started
Developing on devkit include two part:

1. Hardware design, which contains FPGA IP core design, board IO pins map and so on. Before you develop on arm, you must create your hardware system, to provide hardware setting for software. 
   For people who want to focus on arm develop or need a hardware system design reference, robsense provide a prebuild hardware system of devkit, it contains basic ports IP core and settings of arm.
   prebuild hardware path:

   ```
   PhenixPro_Devkit/amp_system/vivado_prj.tar.gz
   ```
**Note:**
    PhenixPro Devkit V2.0 have the same Hardware design（vivado project）as V1.0.

2. Software design, which contains bare-metal, operation system develop on dual arm-cortex a9

