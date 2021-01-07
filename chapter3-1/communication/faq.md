# FAQ

_**"Thanks again for your support of Robsense products!Your every question and feedback, is the trust and expectation of us.We go all out to provide you with good service."                                                                     - Robsense technical support team**_

**Question 1**:After networking according to the operation manual on the official website, the corresponding node cannot be identified.  
**Answer**:  
1.1 Please check the status of the gateway indicator light. If the light is only green, it shall be processed according to section 2.1.If there are other indicator lights, they can be used normally.  
1.2 Please use the manual to see if you can use the EasySwarm personal software: SETTING -- Gateway -- whitelist will be added correctly.  
1.3 Please download and install the serial port assistant software, connect the node with Micro usb interface, identify the MAC address of the node , and check whether the gateway white list is added correctly.  
1.4 If the MAC address of the node cannot be obtained, the firmware of the node can be re-written to reset the MAC of the node to FDFD0001. Please refer to section 2.1 for the specific operation.  
1.5 Please confirm that the gateway whitelist has been added correctly according to the operation manual.  
1.6 If the above attempts fail to solve the problem, please send the relevant equipment back to Robsense after-sales department for processing. For the specific process, please consult Robsense after-sales specialist.

**Question 2**:How to update the firmware for gateway and node?  
**Answer**:  
2.1 You can download the gateway and node firmware from the official website, purchase the j-link emulator by yourself, and then get the j-link driver and how to use the compressed package for free from Robsense after-sale service.  
2.2 If you can't update the firmware by yourself or you can't judge the specific problem, please send the relevant equipment back to Robsense after-sales service for processing. For specific operation, please get the confirmation of Robsense after-sales service before proceeding.

**Question 3**:How to deal with packet loss or disconnection in node detection?  
**Answer**:  
3.1 When the gateway communicates with the node normally, the node detection packet loss rate is 0, which is detected once every second.When the flight control is written as APM/PX4 official firmware, there is a case of serial data incompatibility, which may cause packet loss or disconnection.Other flight control firmware may have poor data compatibility.  
3.2 We recommend the use of PX4 firmware, and provide px4fmu-v2\_default.px4 firmware, and users can cooperate with PIXHAWK V2.4.8 version of flight control to verify the communication of swarmlink set.  
3.3 Users can view the communication situation of the swarmlink suite offline to solve the problem of equipment failure, such as using the mobile phone 5V charger to connect the android data line to power the nodes, and then connecting the gateway to the EasySwarm personal version to test the communication situation of the nodes online.  
3.4 If the user open source flight controller for secondary development, there is likely to be a case of serial data incompatibility, please contact the sales staff to discuss technical support.

**Question 4**:In the node packet loss rate test, the received quantity is greater than the sent quantity.  
**Answer**:  
4.1 This is a reply mechanism during node startup and does not affect usage.

**Question 5**:How to start swarms flight.  
**Answer**:  
5.1 Read the operation manual thoroughly and be familiar with each operational process of EasySwarm personal edition and understand it effectively.  
5.2 It is necessary for professional operators to use remote control or other tools to verify the reliability of fixed-point flight function for the flight participating in swarms.  
5.3 Individual flight tests were conducted for each route in the swarms files using reliable and protective aircraft to verify that each route designed could be implemented normally. Familiar with the use of the personal version of EasySwarm.  
5.4 Note the flight trend of each route to determine the placement of aircraft executing that route.  
5.5 After confirming that the MAC of each node participating in the flight is set correctly, the aircraft is arranged according to the flight trend of each route and sufficient safety distance is reserved.In the verification stage, more safety distance can be reserved and pause can be taken when.  
5.6 Once again, confirm that the designed route is correct, and apply the flight plan to the personal version of EasySwarm to start the swarms flight.

**Question 6**:use real-time location feedback for aircraft in the personal version of the software.  
**Answer**:  
6.1 SwarmLink only supports personal version of EasySwarm. If you need real-time location feedback, please purchase our Swarm Pack, which is standard with enterprise version of EasySwarm and supports it.For details, please contact Robsense sales team.

**Question 7**:According to the manual to repair the code for secondary development, can not use the gateway, nodes and other functions.  
**Answer**:  
7.1 Due to the technical challenge of modifying the flight control code, we cannot confirm whether your development work is effective. Please ask for help from our WeChat group or dev.robsense.com developer BBS.It is recommended that you detail your development and problem details so that developers with the same experience can understand your problem and help.However, we cannot guarantee that you can get 100% support. Although it is not within the scope of after-sales service, Robsense will try its best to help you find problems and solutions brought by development.

**Question 8**:After the secondary development of the ardupilot firmware, packet loss still exists in the gateway and node test.  
**Answer**:  
8.1 as question 7.  
8.2 Robsense's experience: the problem may be caused by the congestion caused by the large amount of data sent to the gateway actively by the flight control through the node.If the cause of the failure needs to be confirmed, it is recommended to turn on the packet capture software \(for example, Device Monitoring Studio\) at the gateway side to see if large amounts of data are received from the node without any active requests being made.If the situation described above is met, it can be positioned as a problem caused by flight control, and the positioning problem in the development process needs to be reviewed.

**Question 9**:Using pixhawk v2 flight control and px4fmu-v2\_default.px4 firmware, the packet loss rate is high and cannot be controlled when swarmlink is connected.  
**Answer**:  
9.1 Confirm whether the flight control hardware version used can normally match the px4fmu-v2\_default.px4 firmware.  
9.2 Verify that the firmware is written into the flight control process correctly.

**Question 10**:Cannot use gh4p-gh4p wire provided in the kit.  
**Answer**:  
Please contact Robsense after-sales department to confirm the flight control hardware version to get the corresponding line sequence diagram.

**Question 11**:When using swarms files to perform swarm flight, the flight trajectory deviated greatly from the expected one.  
**Answer**:  
11.1 Use the stop function in time and operate the aircraft to return in time.  
11.2 Check whether the filled coordinates of the base point are wrong or not.  
11.3 Multiple aircraft were used to verify that the collected base point were correct.  
11.4 High precision base station\(like RTK\) is used to collect the coordinates of the base point, and the safety flight verification of the single aircraft is carried out.  
11.5 You can upgrade the EasySwarm enterprise version through commercial channels to directly collect the real-time location of the aircraft.

**Question 12**:There are two 0001 nodes in the gateway whitelist.  
**Answer**:  
12.1 After disconnecting all online nodes, clear the white list, and then add the white list again  
12.2 Please send the relevant equipment back to Robsense after-sales service for processing. The specific operation shall be conducted after the confirmation of Robsense after-sales service.

**Question 13**:Early use of EasySwarm V1.0 software, modify the node MAC mistakenly input as FCFC0001.After switching to V2.0, the software could not identify the node.  
**Answer**:  
13.1 Please use V1.0 version to modify the MAC, but the 1.0 version is not stable, the modification success rate is low, Robsense can help you complete the update.  
13.2 You can also use j-link to refresh the node firmware with the official website information. Robsense can help you to complete the firmware update.  
13.3 Or you can send SwarmLink to our company and we will help you complete the update.

**Question 13**:If the flight control hardware we are using is not officially supported by Robsense, can you guide us to complete the development?  
**Answer**:  
The development work belongs to the technical consultation and the technical service scope, please contact our commercial colleague, we wholeheartedly serve for you.

