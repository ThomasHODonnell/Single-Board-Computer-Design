# **Images**

- this folder will house screenshots of PCB Schematics to demonstrate progress and organize logic. 

## SINGLE-BOARD COMPUTER (as of July 2, 2023)
### 1. Initial Power System
- I am using a Power Management IC. 
- These circuits create voltages needed to supply main power IC. 
- have not created sodder pads for battery input 

![alt text][InitialPower]
[InitialPower](PCBs/SchematicImages/Images/Batt2PowerIC.png "Battery->PowerIC")


### 2. Power Management IC
- This IC will power every other IC in the SBC
- MPU, RAM, EMMC, USB-C, SD
  
![alt text][PowerIC]
[PowerIC](PCBs/SchematicImages/Images/PowerManagementIC.png "Power Management IC")


### 3. MPU (unfinished)
- Main Component of the SBC
- Currently connected to most of the minimum requirements

![alt text][MPU]
[MPU](PCBs/SchematicImages/Images/MPU.png "MPU")


### 3. Battery Level Gauge (unfinished)
- This IC will be used primarily for ARM Programming testing when I get the board. 
  - I have little experience with ARM Programming. I can test different techniques on an IC that is relativly simple to program. 
  - compared to the MPU ... 

![alt text][BattGauge]
[BattGauge](PCBs/SchematicImages/Images/BatteryGaugeIC.png "Battery Gauge IC")



### 4. USC-C Receptacle
- Will be used for loading programs on to the SBC. 

![alt text][USBC]
[USBC](PCBs/SchematicImages/Images/USBC.png "USB-C Receptacle")



### 5. SD Card Receptacle (unfinished)
- Will be used to load X-Linux-AI onto the SBC. 

![alt text][SD]
[SD](PCBs/SchematicImages/Images/SD.png "SD Card Receptacle")

### 7. Entire Schematic (not sure which external RAM, EMMC, as seen in bottom left)

![alt text][Full]
[Full](PCBs/SchematicImages/Images/Full7.2.23.png "Full Schematic Image")
