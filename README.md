# DC Motor Generator Monitoring and Control System

> Real-time embedded system for controlling and monitoring a reversible DC motor-generator set using an Arduino Nano ESP32.

---

# Overview

This project was developed as part of an Embedded Systems laboratory project with the objective of demonstrating the reversible operating principle of DC machines.

The developed platform is capable of controlling two mechanically coupled DC motors while monitoring their electrical behaviour in real time.

The system measures voltage and current, calculates electrical power, identifies the operating mode of each motor (Motor, Generator or Stopped), and displays all relevant information through a 16x2 LCD interface.

The system can be fully controlled using either physical push-buttons or commands sent through the Serial Monitor.

---

# Project Objectives

- Demonstrate the reversibility of DC machines.
- Control two mechanically coupled DC motors.
- Measure voltage and current in real time.
- Calculate electrical power.
- Identify the operating mode of each machine.
- Display electrical measurements on an LCD.
- Develop an embedded application using an Arduino Nano ESP32.
- Integrate sensors, actuators and embedded software into a single system.

---

# Development Process

This project followed an iterative engineering approach.

## Phase 1 — Initial Prototype

The first version was assembled on a breadboard to validate:

- Motor control
- Voltage sensing
- Current sensing
- LCD communication
- PWM generation
- Embedded firmware

*(Insert Breadboard Prototype Image)*

---

## Phase 2 — Hardware Assembly

After validating the circuit, all components were transferred to a prototyping PCB.

The electronics were soldered and mechanically reinforced to improve reliability.

*(Insert PCB Assembly Image)*

---

## Phase 3 — Final Prototype

The final system integrates:

- Arduino Nano ESP32
- L298N motor driver
- Voltage sensors
- Hall-effect current sensors
- LCD display
- Push buttons
- Dual DC motor-generator assembly

*(Insert Final Prototype Image)*

---

# Features

- Bidirectional DC motor control
- PWM speed control (20 kHz)
- Real-time voltage measurement
- Real-time current measurement
- Electrical power calculation
- Automatic operating mode detection
- LCD user interface
- Physical push-button control
- Serial Monitor interface
- Hall sensor calibration
- Real-time monitoring

---

# Hardware

| Component | Description |
|------------|-------------|
| Arduino Nano ESP32 | Main embedded controller |
| L298N | Dual H-Bridge motor driver |
| 2 × DC Geared Motors | Motor / Generator demonstration |
| Funduino Voltage Sensor | Voltage measurement |
| ACS70331 Hall Sensor | Current measurement |
| LCD 16x2 I2C | User interface |
| Push Buttons | Local control |
| LEDs | Operating status indication |
| 12 V Power Supply | System power source |

---

# Software

- Arduino IDE
- C++
- Embedded Programming
- PWM Control
- ADC Data Acquisition
- Serial Communication

---

# System Architecture

```
                +-------------------------+
                | Arduino Nano ESP32      |
                +------------+------------+
                             |
      +----------------------+----------------------+
      |                      |                      |
 Voltage Sensor      Current Sensor         Push Buttons
      |                      |                      |
      +----------------------+----------------------+
                             |
                   Embedded Control Software
                             |
             +---------------+----------------+
             |                                |
       LCD Interface                  PWM Generation
             |                                |
             +---------------+----------------+
                             |
                      L298N Driver
                             |
                  DC Motor ↔ DC Generator
```

---

# Operating Principle

The system consists of two mechanically coupled DC motors.

When one motor is powered, it converts electrical energy into mechanical energy, causing the second motor to rotate.

The second machine then operates as a generator, converting mechanical energy back into electrical energy.

Because DC machines are reversible, either motor can operate as a motor or as a generator depending on the selected operating mode.

---

# User Interface

The system can be controlled in two different ways.

## Physical Interface

- Push Button A
- Push Button B

These buttons allow the user to:

- Start or stop each motor
- Change operating modes

---

## Serial Monitor Interface

The Serial Monitor provides additional functionality.

| Command | Description |
|----------|-------------|
| `1` | Toggle Motor A |
| `2` | Toggle Motor B |
| `0` | Stop both motors |
| `A=xxx` | Set PWM duty cycle for Motor A |
| `B=xxx` | Set PWM duty cycle for Motor B |
| `s` | Print system status |
| `c` | Calibrate Hall sensors |
| `h` | Display help menu |

---

# Measurements

The embedded firmware continuously acquires:

- Voltage
- Current

The measured values are processed to calculate:

- Electrical Power

All measurements are updated in real time and displayed on the LCD.

---

# Engineering Concepts Applied

- Embedded Systems
- Motor Control
- PWM Generation
- ADC Data Acquisition
- Hall-effect Current Sensing
- Voltage Measurement
- Sensor Calibration
- Electrical Instrumentation
- Real-Time Programming
- Hardware Integration
- Embedded Debugging

---

# Repository Structure

```
dc-motor-generator-monitoring-system

├── src/
├── include/
├── documentation/
├── images/
├── schematics/
├── results/
├── README.md
└── LICENSE
```

---

# Results

The developed platform successfully demonstrates:

- DC machine reversibility
- Embedded motor control
- Electrical parameter monitoring
- Sensor integration
- PWM speed control
- Embedded software development
- Hardware and software integration

The project provided valuable experience in electronics, embedded programming, instrumentation and debugging.

---

# Challenges

Several engineering challenges were encountered during development.

- Hall sensor calibration
- Electrical noise
- PWM tuning
- LCD communication
- Embedded debugging
- Hardware integration
- Mechanical coupling of both motors

These challenges were progressively solved through testing, calibration and iterative hardware improvements.

---

# Future Improvements

Possible future developments include:

- PID speed control
- Closed-loop motor control
- SD card data logging
- Wi-Fi remote monitoring
- Bluetooth communication
- Web dashboard
- Mobile application
- Industrial communication protocols (Modbus RTU)
- Real-time data visualization
- Efficiency analysis of the motor-generator set

---

# Skills Demonstrated

| Area | Skills |
|------|--------|
| Embedded Systems | Arduino Nano ESP32 |
| Programming | C++ |
| Electronics | Analog Signal Acquisition |
| Control | PWM Motor Control |
| Instrumentation | Voltage & Current Measurement |
| Hardware | PCB Assembly & Soldering |
| Debugging | Embedded Hardware & Software |
| Integration | Sensors, Drivers and User Interface |

---

# Gallery

## Breadboard Prototype

*(Insert Image)*

---

## PCB Assembly

*(Insert Image)*

---

## Final Prototype

*(Insert Image)*

---

## Testing

*(Insert Image)*

---

# License

This project is released under the MIT License.

---

# Author

**Tomás Ferreira**

Electrical & Telecommunications Engineering Student

University of Aveiro

Interested in:

- Industrial Automation
- Embedded Systems
- Robotics
- Electronics
- Control Engineering
- Industry 4.0

Feel free to explore my other engineering projects and connect with me on LinkedIn.

Here are some of the images of the progress of the project:

![Project Status](https://img.shields.io/badge/Status-Completed-success)

<img width="1536" height="2048" alt="WhatsApp Image 2026-07-11 at 16 36 11" src="https://github.com/user-attachments/assets/bcb6544f-d900-47cd-97e0-d10b72d2f42c" />

![Platform](https://img.shields.io/badge/Platform-Arduino%20Nano%20ESP32-blue)

<img width="1536" height="2048" alt="WhatsApp Image 2026-07-11 at 16 36 12" src="https://github.com/user-attachments/assets/f4b828c5-a2db-49d4-bb51-aae858a4e45f" />

![Language](https://img.shields.io/badge/Language-C%2B%2B-orange)

# License

This project is licensed under the MIT License. See the LICENSE file for more information.
# Author

**Tomás Ferreira**

Electrical & Telecommunications Engineering Student  
University of Aveiro

Areas of Interest:
- Industrial Automation
- Embedded Systems
- Robotics
- Control Engineering
- Electronics
- Industry 4.0

## Contact
- Email: ferreiratomas994@gmail.com
- Outlkook tomasff52@ua.pt
- LinkedIn: (https://www.linkedin.com/in/tomas-ferreira-52635a2b8/?isSelfProfile=true)
- GitHub: https://github.com/teu-utilizador



<img width="1536" height="2048" alt="WhatsApp Image 2026-07-11 at 16 36 12 (1)" src="https://github.com/user-attachments/assets/b15caf7b-5eb3-4511-9c9f-6704e003cbb4" />


![License](https://img.shields.io/badge/License-MIT-green)
