# Hardware Components

## Main Components

| Component | Function |
|---|---|
| MPU6050 | Measures acceleration and angular velocity for tilt estimation |
| Arduino Nano | Microcontroller used to process sensor data |
| ESP32 | Alternative microcontroller explored during development |
| L298N | Dual H-bridge motor driver |
| DC Motors | Drive the two wheels and provide corrective movement |
| HC-SR04 | Ultrasonic obstacle detection |
| HC-05 | Bluetooth communication |
| Li-ion Battery | Provides power to the system |
| DC-DC Buck Converter | Regulates the supply voltage |

## System

The hardware consists of sensing, processing, motor-control, power, and communication components.

The MPU6050 provides the motion data required for balancing. The microcontroller processes the sensor information and generates control signals for the L298N motor driver. The motor driver controls the DC motors.

The project also included an HC-SR04 ultrasonic sensor for obstacle detection and an HC-05 Bluetooth module for communication.

## Development Hardware

Different microcontrollers and electronic components were tested during development. The project encountered hardware issues including ESP32 bootloader problems, voltage regulator failures, Arduino Nano issues, and Arduino Uno problems.

Components and PCB/soldering arrangements were subsequently changed during troubleshooting and testing.
