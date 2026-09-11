# System Architecture

The self-balancing robot consists of sensing, processing, control, motor, power, and communication subsystems.

## Control Flow

```text
MPU6050
   ↓
Microcontroller
   ↓
Tilt Estimation
   ↓
PID Controller
   ↓
L298N Motor Driver
   ↓
DC Motors
   ↓
Corrective Movement
   ↺

Main Subsystems
1. Sensor Subsystem

MPU6050

Measures acceleration and angular velocity and provides the sensor data required for tilt estimation.

HC-SR04

Used for obstacle detection.

2. Control Subsystem

The microcontroller processes sensor information and uses a PID-based feedback approach to calculate corrective motor actions.

3. Motor Subsystem

The L298N motor driver controls the direction and speed of the DC motors.

4. Communication Subsystem

The HC-05 Bluetooth module was intended to provide wireless communication and remote control capabilities.

5. Power Subsystem

The robot uses a Li-ion battery supply with a DC-DC buck converter for voltage regulation.

Overall System

The robot continuously uses sensor feedback to estimate its state and generate motor corrections. This closed-loop approach is essential for maintaining the robot's balance.
