# Power Board 2

## Overview
The Autonomous Underwater Vehicle Interdisciplinary Club (AUVIC) competes in an annual international competition where teams build autonomous underwater vehicles (AUVs) to complete an underwater obstacle course. AUVIC is in need of a new power and battery management board(PMB) for the 2021 Autonomous Underwater Vehicle (AUV).

## Specifications
The new PMB is divided into four subsections. The requirements for each subsection are outlined in the following sections.

### 3.1	Battery Management
- Should have a input voltage range of 18V to 28V.
- Should use two 6 cell LiPo batteries as its power source.
- Should have the ability to run the two batteries in parallel.
- Each battery should have fuses. Regular sized automotive fuses are recommended.
- Should have LEDs to indicate if the battery is connected.
- Should have the ability to monitor battery pack voltage, individual cell voltage and pack current.

### 3.2	Power Distribution
- Should have the following power outputs for external systems:
  - 5V at 8A.
    - LCD board - 4A*
    - Inertial Measurement Unit (IMU) - 500mA
    - Hydrophones - 250mA*
    - Torpedo 5V electronics - 250mA*
    - Motor controller 5V electronics - 250mA*
    - Buffer for unplanned boards - 2.75A
  - 12V at 8A.
    - Doppler Velocity Log (DVL) - 3A
    - Ball dropper and grabber arm - 3A*
    - Buffer for unplanned boards - 2A
  - 16V at 3A.
    - Nvidia Jetson TX2 and peripherals - 3A
  - VBatt (22.2V nominal) at 60A continuous.
    - Motor controller - 60A peak
    - Torpedo launcher - 30A for < 1s
- Should be able to switch on/off all external power using the microcontroller.
- Should have the ability to monitor current for each external power output.
- Should have LEDs at each output to indicate if the output is on or off.
- Should have fuses at each output. Regular sized automotive fuses are recommended.

\* = Estimated values.

### 3.3	Microcontroller & Communication
- Should use a STM32F413 microcontroller. 
- Should have a RS232 transceiver to communicate with an IMU.
- Should have LEDs connected to the microcontroller for debugging and to show system status.
- Should use a Controller Area Network (CAN) bus to communicate to external systems.

### 3.4	Sensors
- Should connect to a reed switch to power on/off the AUV.
- Should connect to a water sensor to detect leaks in the vehicle’s housing.
- Should measure internal pressure, temperature, and humidity.
- Should connect to an external water pressure sensor used to determine the AUV’s depth in the water.

## Progress
Schematic completed
Simulations completed
Layout in progress

![Image of layout thus far](https://github.com/uvic-auvic/PCB-Power_Board_2/blob/master/Power_Board_2/3D%20Model/Power_Board_2.png)


