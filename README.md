# Obstacle Avoidance Ground Robot

## Project Report by Aanvik Bhatnagar, Divyansh Pandey, Hemang Jain, Mohak Somani

## 1. Introduction

The project involves the implementation of an intelligent obstruction-avoidance ground robot using the ESP32 micro-controller. The system integrates ultrasonic sensors, motor drivers, edge-avoidance, radar (real-time obstacle visualization through a radar unit), and a Bluetooth Remote control. The embedded system employs a seamless data flow architecture to facilitate communication and control between various components, enabling both autonomous and manual modes of operation for the ground robot. The Radar Unit and Edge Avoidance enhance the overall functionalities of the ground robot from the perspective of safety and applications.

## 2. Component List

1. ESP32 (x2)
2. Chassis with Tyres (x4) and Motors (x2)
3. Motor Driver (x1)
4. HC-SR04 Ultrasonic Sensor (x4)
5. Servo Motor (x1)
6. IR Sensor (x2)
7. LEDs & Breadboards
8. Resistances & Jump Wires
9. Miscellaneous Hardware & Testers

## 3. Calibration

### 3.1 Calibration of IR sensor

The IR sensors require alignment, and the transmitter-receiver pair should be at an appropriate distance to get accurate readings. Calibration involves adjusting the threshold and aligning the sensors as a unit to ensure independent and accurate operation.

### 3.2 Calibration of Ultrasonic Sensor

Mapping actual distances of obstacles and using linear regression to create a function for measured distance calibration.

### 3.3 Calibration of Motor Driver

The motor driver's voltage is controlled by a regulator, and a resistor is added in parallel to limit the current to the ESP, preventing overload.

### 3.4 Calibration of Servo Motor

Adjusting the initial angle of the servo motor to correct for any offset relative to its body.

## 4. Implementation

The implementation includes the assembly of hardware components and firmware development, integrating sensor readings, data communication, motor control, and autonomous/manual control algorithms.

### 4.1 Obstacle Avoidance

Utilizing an array of ultrasonic sensors to detect obstacles, implementing a threshold-based algorithm for obstacle avoidance.

### 4.2 Edge avoidance

Calibrating IR sensors to the height of the car chassis and implementing an edge-avoidance algorithm.

### 4.3 Radar

A radar unit consisting of an ultrasonic server on a servo motor for real-time visualization of obstacles. Data is transmitted wirelessly using OM2M server.

### 4.4 Remote Control

Bluetooth remote control facilitated by the ESP32 and an Android application, allowing manual control over the robot's movement.

## 5. Flowchart

### 5.1 Logical Flowchart of Model

Visual representation of the logical flow of the ground robot's model.

### 5.2 Logical Flow of Code

Flowchart depicting the logical structure of the code.

## 6. Error Analysis

### 6.1 Excess Current to ESP

To prevent excess current to the ESP, a resistor is added in parallel to the outlet of 5V.

### 6.2 Delay Due to OM2M

Uploading and retrieving data from OM2M introduces a latency of about 600 ms, affecting the radar unit's smoothness.

### 6.3 Avoiding Infinite Loop

Preventing infinite loops by adjusting the displacement angle after each cycle of left and right rotation.

### 6.4 MD5 File Error

Addressing file corruption and write protection issues during firmware updates.

### 6.5 Adjusting COM

Correcting instability caused by uneven weight distribution on one side of the robot car.

## 7. Circuit Diagram

### 7.1 Radar Unit

[Circuit diagram for the radar unit.](#)

### 7.2 Motor Driver and Sensors

[Circuit diagram for motor driver and integrated sensors.](#)

## 8. Appendix

### 8.1 Motor Driver and Integrated Sensors Codet

This unit contains the Remote Control , Obstacle Avoidance and Edge Avoidance code .
[Motor Driver and Integrated Sensors Code](#)

### 8.2 Radar Unit Arduino Code

[Radar Unit Arduino Code](#)

### 8.3 Linear Regression Code

[Linear Regression Code](#)

### 8.4 Processing Code

[Processing Code](#)

## 9. References

[References](#)