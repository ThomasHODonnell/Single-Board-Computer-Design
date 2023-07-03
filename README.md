# A.I. Drone M1.0

## **Table of Contents** 
1.  [Summary](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Summary)

2.  [Timeline](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Timeline)

3.  [Functionality](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Functionality)

4.  [Components](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Components)

5. [To-do](https://github.com/ThomasHODonnell/A.I.DroneM1.0#To-do)

6.  [Notes](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Notes)

7. [References](https://github.com/ThomasHODonnell/A.I.DroneM1.0#References)


## **Summary** 
- This project will use the mechanical frame of a retail drone. 
  - Make: DJI
  - Model: Maxis Mini I 
- **I will design my own PCBs** and exchange them for the boards provided with the product. 
  - PCBs will be designed to fit the dimensions, I/O, and performance needs of the Maxis Mini I. 
- **I will create my own firmware.** The firmware will be created such that the drone can run programs in python. 
  - I will not be creating my own compiler or Operating System. 
  - The open source python compiler can be found here: 
    - *Source* =>
- **I will design a neural network(s)** to provide application for the drone. 
  - M1.0 will utilize an object recognition software. 
  - Intended to be a relativly basic deep learning network that can be scaled to fit the applications of MarkN(s) to come. 

## This project is intended to demonstrate profiency in the following areas ...
  - **Electrical Engineering**
    - Analog Circuit Devices
      - RLC, Transistors, Diodes
      - MOSFET, FPGA
    - Digital Electronic Devices
      - Microprocessors / Microcontrollers / IC's
    - PCB Design and Implementation using **KiCad** 
      - Design
      - Simulation (LTSpice)
      - Verification

  - **Computer Science**
    - Assembly Language 
      - Bill of Materials (BOM)
      - Footprint Position File
    - Operating System
    - Machine Learning (TensorFlow)
      - Deep Learning
      - Neural Networks


##  **Timeline**
- M1.0 Final Due Date 
  - September 14, 2023 (LSU Career Expo)
- SBC Due Date
  - July 31, 2023


## **Functionality**
1. boot to a stable state
   1. main power board is operational 
   2. needs to be able to read python code (TF is built into OS)
2. able to hover in place
   1. need to build ERC board 
   2. connect ERC to motors   
3. create flight prog
   1. create GPS/INS (inertial measurement system)
   2. use chip to design flight program via ext. remote. 
4. Integrate progs 
   1. remove ext remote; integrate with python AI. 
      1. need to let AI and  INS chip commuinicate 
      2. will need to program aviodance commands via function(dist.)
      3. apple measurement app 



## **Components (see DS in folder)**
- MPU
  - STM32MP135DAD1
- Power Management IC
  - STMIC1BPQR
- Battery Level Gauge
  - STC3115ITJ
- RAM
  - undecided
- EMMC
  - undecided
- USB-C Receptacle 
  - undecided
- SD Card Receptacle
  - undecided

## **To-do**
1. *finish a SBC* (main power board)
   - SBC to run python code
   -  will need channels for dual communication between INS and ERC boards (sodder pads)
2. *Gather Data for NN*
   - live data feeds to train convergence on, select initial terrain. 


## **Notes**
- *Terms / Concepts I need to learn and research how they need to be integrated in this project.*

## EE
### *PCB Design (3 boards)*
  - Power Distribution and Electronic Speed Control Board
    - DJI uses 'C8051F330' MPU => Silicon Labs 
      - does not appear to be usb capable 
  - GPS / IMU (internal measurement unit) Board 
    - MPU6050
      - gyroscope
      - accelerometer 
    - covers gravitational acceleration, rotational velocity, tempature
    - used in sync with MCU
  - Main Power Board (SBC)



### Firmware
- **EDA** (Electrnic Design Automation) is software and hardware that assist the design process of semiconductor devices or chips => MCU / MPU 
  - used to design and verify the manufacuring process => meets performance needs => monitor performance
  

- **STM** - an EDA software enviornment (will finish schematic before ARM prog.)
  - *setup*
    - select firmware package 
    - C++ as targeted language
    - STM generates code template
    - write ARM prog. for MPU + Batt Gauge.
  - *Design* 
    - Set up the Pinouts based on PCB Design 




### CS
- OS
  - Open Source Linux Distribution
    - flight sys prog interacts with neural network clients
  - Designed to simply run a terminal where a remote will send predefined commands. 
    - *X-Linux-AI* => 
- Deep Learning Algorithm(s)
  - make appx for RAM needed. 
  - Flight System
  - Object Recognition  



## **References**

### General
- https://microchipdeveloper.com/32mpu:harmony3-diff-mcu-mpu 
- https://stm32ai.st.com/ (on-chip NN sensors)

### EE
- https://www.raspberrypi.com/documentation/computers/raspberry-pi.html#schematics-and-mechanical-drawings (rasp sch)
- https://www.st.com/en/microcontrollers-microprocessors/stm32mp153d.html (MPU)
  - MPU Datasheets can be found here ... 
  - https://www.csselectronics.com/pages/can-fd-flexible-data-rate-intro (CAN-FD)
 
### Firmware
- https://github.com/raspberrypi (OS + Assembly)
### CS
- https://www.mathworks.com/help/nav/ug/model-imu-gps-and-insgps.html  (INS prog)
- (https://stm32ai.st.com/ai-for-linux/) (StLinux - AI)
- https://wiki.st.com/stm32mpu/wiki/X-LINUX-AI_OpenSTLinux_Expansion_Package (OS Docs)


### Datasheets (downloadable; personal notes for reference)
- https://www.st.com/resource/en/datasheet/stm32mp153d.pdf (MAIN DS)

