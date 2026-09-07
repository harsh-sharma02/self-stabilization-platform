# 3-Axis Platform Stabilization System

## Overview

This project involved the design and implementation of a three-axis stabilization platform capable of compensating for angular disturbances using inertial sensing and servo-based actuation.

The system combines an **MPU6050 inertial measurement unit (IMU)** with an **ESP32-based controller**, **PCA9685 servo driver**, and three servo actuators.

The MPU6050 provides motion/orientation-related sensor measurements, which are processed by the controller to determine the required actuator response. The servo motors then adjust the platform to compensate for changes in orientation.

The project was developed as a course project with emphasis on embedded systems, sensor interfacing, actuator control, and feedback-based stabilization.

---

## Objectives

The main objectives were:

- Develop a three-axis stabilization mechanism.
- Interface an MPU6050 IMU with a microcontroller.
- Process sensor measurements for platform stabilization.
- Control three servo actuators independently.
- Implement the servo-control interface through a PCA9685 driver.
- Integrate the mechanical, electronic, and software components into a working prototype.
- Evaluate the response of the platform to angular disturbances.

---

## System Architecture

The complete system can be represented as:

```text
              Platform Motion
                    |
                    v
              +-----------+
              |  MPU6050  |
              |    IMU    |
              +-----+-----+
                    |
               Sensor Data
                    |
                    v
              +-----------+
              |   ESP32   |
              | Controller|
              +-----+-----+
                    |
             Calculate Error
                    |
                    v
              +-----------+
              |  PCA9685  |
              |   Driver  |
              +-----+-----+
                    |
          +---------+---------+
          |         |         |
          v         v         v
       Servo 1   Servo 2   Servo 3
          |         |         |
          +---------+---------+
                    |
                    v
              Stabilized Platform
```
---
