# Tarcin Robotics & Embedded Systems Internship 2026

This repository contains my hands-on internship projects, source code, circuit designs, simulation observations, and technical learning notes.

## Task 01 — Sounding Sentry Guard
**Reference:** Aries Advanced — Task 141

### Project overview
A sensor-based security alert prototype using an HC-SR04 ultrasonic sensor, PIR motion sensor, buzzer, and 16x2 I2C LCD with the VEGA ARIES board.

### Components and connections

| Component | Signal | VEGA ARIES pin |
|---|---|---:|
| HC-SR04 | TRIG | D14 |
| HC-SR04 | ECHO | D15 |
| PIR sensor | OUT | D17 |
| Buzzer | Signal | D12 |
| LCD 16x2 | I2C | I2C interface |

### Observed simulation output
- When the PIR simulation control is activated, the Serial Monitor displays an intruder alert and the buzzer output becomes HIGH.
- When the PIR simulation control is inactive, the Serial Monitor displays the secure status.
- The observed alert output included: `ALARM - Intruder Detected! Distance: 0 cm | Motion: 1`.

### Source code
See [Task_01_Sounding_Sentry_Guard.ino](Task-01-Sounding-Sentry-Guard/Code/Task_01_Sounding_Sentry_Guard.ino).

### MbedO workspace
[Open the Task 01 MbedO workspace](https://mbedo-dev.tarcin.in/designer/p/8d8c7342-69f2-4169-8a5c-30d8cb8fa5a7/project-1).

---
More internship tasks will be added as they are completed.
