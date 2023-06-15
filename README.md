# A.I. Drone M1.0

## **Table of Contents** 
1.  [Summary](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Summary)

2.  [Timeline](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Timeline)

3.  [Notes](https://github.com/ThomasHODonnell/A.I.DroneM1.0#Notes)


## **Summary** 
- This project will use the mechanical frame of a retail drone. 
  - Make: DJI
  - Model: Maxis Mini I 
- **I will design my own PCBs** and exchange them for the boards provided with the product. 
  - PCBs will be designed to fit the dimensions, I/O, and performance needs of the Maxis Mini I. 
- **I will create my own firmware.** The firmware will be created such that the drone can run programs in python. 
  - I will not be creating my own compiler. 
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
    - Microprocessors / Microcontrollers
    - PCB Design and Implementation using **KiCad** 
      - Design
      - Simulation
      - Verification

  - **Computer Science**
    - Assembly Language 
      - Bill of Materials (BOM)
      - Footprint Position File
    - Operating System?
    - Machine Learning 
      - Deep Learning
      - Neural Networks


##  **Timeline**
- M1.0 Final Due Date 
  - September 14, 2023 (LSU Career Expo)



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
  - Main Processing Core Board 


### Firmware
- **EDA** (Electrnic Design Automation) is software and hardware that assist the design process of semiconductor devices or chips => MCU / MPU 
  - used to design and verify the manufacuring process => meets performance needs => monitor performance
  

- **STM** - an EDA software enviornment
  - *setup*
    - select the chip that meets needs
    - select firmware package 
    - C/C++ as targeted language
    - STM generates code template
  - *Design* 
    - Set up the Pinouts based on PCB Design 

### CS
- OS
  - Open Source Linux Distribution
  - Designed to simply run a terminal where a remote will send predefined commands. 
    - *Source* => 
- Deep Learning Algorithm(s)
