## PhenixPro Devkit Release Note

---

Phenix Devkit Firmware v0.1 Mar 26 12:19:31 2017

First version \(git commit 3a4a65\)

1. Support copter self-stabilization flight mode
2. Support sbus remote control receiver
3. Compatible with common ground station: Mission Planner/APM Planner/QGround

---

Phenix Devkit Firmware v0.2 Apr 19 16:34:59 2017

Changes from 0.1

1. Change serial IP core from uartlite to uart16550, which can change baudrate
2. Support GPS and alt hold flight mode
3. Support log record during flight
4. Fix crash problem, update FreeRTOS version to v9.0.0,  old version FreeRTOS can not support saving FPU context in task switch, it cause fatal float error in EKF





