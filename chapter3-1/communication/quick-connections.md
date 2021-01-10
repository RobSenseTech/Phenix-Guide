# Quick Connections

![Quick Connections](../../.gitbook/assets/Quick%20Connections.png)  
System settings in the function is still perfect, can only use the modified mac address.  
**STEP 1** Connect RobSense Phenix Pro's Serial1 port with SwarmLink node UART port.  
**STEP 2** Connect SwarmLink Gateway micro USB with ground station.  
**STEP 3** Select the ground station serial number, baud rate, click open serial port.

## Hardware parameters

CPU：ARM Cortex-M3  
Working frequency：433MHz  
Channel bandwidth：500KHz  
Modulation mode：LoRa spread spectrum  
Transmit power：20dBm  
Receiving sensitivity : -148dBm  
Working voltage：5V  
Working current：50mA  
Working temperature：-40℃-+85℃  
Interface：CAN，MicroUSB，LAN  
Size：60mm_37mm_11mm  
Weight：20g  
![Hardware parameters](../../.gitbook/assets/Hardware%20parameters.png)  
SwarmLink Node/Gateway：1.TXD 2.RXD 3.VCC 4.GND

## Flight Controller Configuration \(PX4 1.7.3\)

If the developer is using px4-1.7.3 version, there is need to modify original firmware. The red boxes below show the code to be modified or added.  
**Mavlink update:**  
![Mavlink update01](../../.gitbook/assets/Mavlink%20update01.png) 
![Mavlink update02 | 50%](../../.gitbook/assets/Mavlink%20update02.png) 

1.Find the firmware/SRC/module/mavlink/mavlink\_main.cpp file.  
2. Add code in the corresponding position, as shown in the 1, 2, 3, 4 and 5 steps shown above.  
**Turn off serial port flow control:**  
![Turn off serial port](../../.gitbook/assets/Turn%20off%20serial%20port.png)  
1.Find the firmware/SRC/module/mavlink/mavlink\_main.h file.  
2. Add code in the corresponding position, as shown in the 1 steps shown above.  
3.Find the firmware/SRC/module/mavlink/mavlink\_main.cpp file.  
4. Add code in the corresponding position, as shown in the 2,3,4 steps shown above.  
**Modify boot file:**  
![Modify boot file](../../.gitbook/assets/Modify%20boot%20file.png) 1.find firmware/ROMFS/px4fmu\_common/init.d/rcS file.  
2. add the code at the corresponding location, as shown in the red area above.


