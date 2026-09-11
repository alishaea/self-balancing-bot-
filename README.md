 # Self-Balancing Robot 🤖

A two-wheeled self-balancing robot developed as a robotics and control-systems project. The robot is designed around the inverted pendulum principle, using sensor feedback and a feedback control system to maintain its upright position.

## 📌 Project Overview

A self-balancing robot continuously detects its tilt and adjusts the movement of its wheels to prevent itself from falling.

The project combines:

- Embedded systems
- Robotics
- Sensor integration
- Motor control
- PID control
- Mechanical design
- Real-time feedback systems

The main objective was to develop a two-wheeled robot capable of maintaining dynamic balance while integrating additional sensing and communication capabilities.

## 🎯 Objectives

- Develop a two-wheeled self-balancing robot.
- Detect the robot's tilt using an IMU.
- Implement feedback-based motor control.
- Apply PID control for balancing.
- Integrate the motor driver and DC motors.
- Explore obstacle detection using an ultrasonic sensor.
- Explore wireless control using Bluetooth.
- Gain practical experience in robotics, embedded systems, and control systems.

## ⚙️ How the Robot Works

The robot follows a closed-loop feedback system:

**MPU6050 → Microcontroller → Tilt Estimation → PID Controller → L298N → DC Motors**

1. The MPU6050 collects acceleration and gyroscope data.
2. The microcontroller processes the sensor data.
3. The robot estimates its tilt angle.
4. The PID controller calculates the required corrective response.
5. The motor driver receives the control signal.
6. The DC motors adjust the wheel movement.
7. The process continuously repeats to maintain balance.

This allows the robot to make continuous corrective movements instead of relying on a fixed motor speed.

## 🔧 Hardware Components

| Component | Purpose |
|---|---|
| MPU6050 | Measures acceleration and angular velocity for tilt estimation |
| Arduino Nano | Microcontroller for processing sensor data and controlling the robot |
| ESP32 | Alternative microcontroller explored during development |
| L298N Motor Driver | Controls motor direction and speed |
| DC Motors | Provide movement and corrective action |
| HC-SR04 Ultrasonic Sensor | Obstacle detection |
| HC-05 Bluetooth Module | Wireless communication and remote control |
| Li-ion Battery | Power supply |
| DC-DC Buck Converter | Voltage regulation |
| Two Wheels | Provide movement and balancing |

## 🧠 PID Control

The robot uses the concept of a PID controller to generate corrective motor actions.

PID consists of three terms:

### Proportional (P)

Responds to the current difference between the desired and actual tilt angle.

### Integral (I)

Accounts for accumulated error over time and can help reduce steady-state error.

### Derivative (D)

Responds to the rate at which the error is changing and helps reduce overshoot.

The general PID equation is:

```text
Output = Kp × e(t) + Ki × ∫e(t)dt + Kd × de(t)/dt
Where:

e(t) = difference between desired and actual tilt
Kp = proportional gain
Ki = integral gain
Kd = derivative gain

The controller uses the estimated tilt to determine how the motors should respond.

📡 Sensor Fusion

The MPU6050 combines an accelerometer and gyroscope.

The accelerometer can be used to determine orientation but is sensitive to vibration and noise.

The gyroscope measures rotational movement but can experience drift over time.

A complementary filter can combine the two measurements to obtain a more stable tilt estimate.

The complementary filter is computationally lightweight and suitable for microcontrollers used in robotics applications.

🔌 System Architecture
                    ┌──────────────────┐
                    │     MPU6050      │
                    │ IMU Sensor       │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │  Microcontroller │
                    │ Arduino / ESP32  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Tilt Estimation  │
                    │ & Sensor Fusion  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │  PID Controller  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │   L298N Driver   │
                    └───────┬───┬──────┘
                            │   │
                     ┌──────▼─┐ ┌▼──────┐
                     │ Motor  │ │ Motor │
                     │  Left  │ │ Right │
                     └────────┘ └────────┘


        ┌─────────────────┐
        │    HC-SR04      │
        │   Ultrasonic    │
        └────────┬────────┘
                 │
                 ▼
          Microcontroller


        ┌─────────────────┐
        │     HC-05       │
        │    Bluetooth    │
        └────────┬────────┘
                 │
                 ▼
          Microcontroller
🏗️ Mechanical Design

The robot was designed as a compact two-wheeled structure suitable for self-balancing.

The mechanical design focused on:

Lightweight construction
Stable chassis design
Proper motor and wheel placement
Suitable center of gravity
Compact electronics arrangement
Accessibility for maintenance and testing

The chassis design was explored using CAD tools, including SolidWorks.

🧪 Prototyping and Development

A circuit prototype was also prepared using Tinkercad during the development process.

The project involved multiple stages of hardware testing, integration, troubleshooting, and component replacement.

Development challenges included:

ESP32 bootloader issues
Voltage regulator failure
Arduino Nano issues
Arduino Uno hardware issues
PCB and soldering problems
Replacement of electronic components
Sensor and motor integration
Control-system tuning

These challenges required repeated testing and troubleshooting before progressing with the robot.

🔬 Testing

Testing involved working with the robot's:

Sensor readings
Motor response
Balance behaviour
Control parameters
Hardware connections
Power system
Mechanical structure

Temporary testing arrangements were considered to reduce the risk of damage while tuning the balancing system.

🚧 Current Scope

The core project focuses on understanding and implementing:

Two-wheeled robotic balancing
IMU-based tilt detection
Feedback control
PID-based stabilization
Motor control
Embedded programming
Hardware integration

Some additional capabilities such as Bluetooth-based remote control and obstacle detection were part of the project's intended system design and development scope.

🚀 Future Improvements

Potential future improvements include:

Encoder-based motor feedback
Improved PID tuning
More advanced sensor fusion
Autonomous navigation
Improved obstacle avoidance
AI-assisted control
Improved wireless control
Better mechanical stability
Improved power management
📚 Learning Outcomes

This project provided practical experience in:

Robotics
Embedded systems
Microcontrollers
PID control
Sensor integration
IMU data processing
Motor control
Hardware troubleshooting
Mechanical design
Circuit prototyping
Real-time feedback systems
📷 Project Images

Project photographs, electronics images, testing photographs, and other development documentation will be added to this repository.

👥 Project

Developed as a robotics and embedded-systems project with a focus on self-balancing control, sensor feedback, motor control, and hardware integration.



