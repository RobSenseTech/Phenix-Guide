# Introducing Phenix Personal Edition

The Phenix Personal Edition is an intelligent control, computing and networking platform for unmanned systems. It integrates a Xilinx Zynq SoC, which packaging a dual core ARM Cortex-A9 CPU and FPGA fabric on a signal chip.

Below shows some differences between Phenix Pro Devkit V1.0 and V2.0. PhenixPro Devkit V1.0 is also running PhenOS\(based on freeRTOS\) and Linux on each CPU core respectively. PhenixPro Devkit V2.0 is running only Linux on dual CPU core. A ArduPilot flight control stack is running as a linux task. Choose according to your interest.

As the version progresses,we mainly use version PhenixPro Devkit 2.0 now.If you want to know more about PhenixPro Devkit V1.0,you can see: [https://github.com/RobSenseTech/PhenixProDevkit1.0](https://github.com/RobSenseTech/PhenixProDevkit1.0)

And all blow introduction is based on PhenixPro Devkit 2.0. Before you start to read the instructions blow,to avoid creating a lot of unnecessary problems,you'd better have some basic knowledge about linux file system,Compiling method,and Xilinx Vivado\SDK usage method.It's easy to search online.

Attitude estimation, flight control, navigation are implemented by ArduPilot flight control stack \([http://ardupilot.org](http://ardupilot.org)\). So far, it only support quadcopter, we call it flying robot.

* The codebase is hosting on github: [https://github.com/RobSenseTech/PhenixPro\_Devkit.git](https://github.com/RobSenseTech/PhenixPro_Devkit.git).
* The developers' guide is presenting on: [https://guide.robsense.com/](https://guide.robsense.com/).
* and hosting on github: [https://github.com/RobSenseTech/PhenixPro-DevKit-Guide.git](https://github.com/RobSenseTech/PhenixPro-DevKit-Guide.git), so developers can contribute to edit and push modifications.
* Developers can push questions to DevKit user forum at: [http://dev.robsense.com](http://dev.robsense.com)

Robsense.com

