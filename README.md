# Tarcin Robotics & Embedded Systems Internship 2026

A hands-on collection of robotics, embedded systems, sensor interfacing, motor control, and simulation tasks completed during the Tarcin internship.

## Repository contents

Each task is organized in its own folder and should include, where available:
- Source code and a short project overview
- Components and pin connections
- Simulation screenshots / observed output
- Testing notes, limitations, and known issues

## Task 01 — Sounding Sentry Guard

**Reference:** Aries Advanced — Task 141  
**Board / environment:** VEGA ARIES v2 / MbedO

### Overview

A sensor-based security-alert prototype using an HC-SR04 ultrasonic sensor, a PIR motion sensor, a buzzer, and a 16×2 I²C LCD.

### Components and connections

| Component | Signal | Board pin |
|---|---|---:|
| HC-SR04 | TRIG | D14 |
| HC-SR04 | ECHO | D15 |
| PIR sensor | OUT | D17 |
| Buzzer | Signal | D12 |
| 16×2 LCD | I²C | I²C interface |

### Observed behaviour

- Activating the PIR simulation control produced an intruder-alert message and set the buzzer output HIGH.
- With the PIR control inactive, the Serial Monitor displayed a secure-status message.
- One observed alert message reported `Distance: 0 cm` while motion was detected. This value should not be treated as a verified ultrasonic measurement.

### Known limitations

- The supplied ARIES v2 simulation/runtime did not provide working support for the Arduino-style `pulseIn()` and `delayMicroseconds()` calls used by the ultrasonic measurement logic.
- PIR-triggered alert behaviour was observed, but ultrasonic distance measurement was not successfully verified in the supplied simulation.
- Therefore, the complete sensor system is **partially tested**, not fully validated.

### Project files

- Source code: [Task 01 Arduino source](Task-01-Sounding-Sentry-Guard/Code/Task_01_Sounding_Sentry_Guard.ino)
- MbedO workspace: [Open Task 01 workspace](https://mbedo-dev.tarcin.in/designer/p/8d8c7342-69f2-4169-8a5c-30d8cb8fa5a7/project-1)

---

## Validation status

| Area | Status |
|---|---|
| PIR alert path | Observed in simulation |
| Buzzer alert output | Observed in simulation |
| Ultrasonic distance measurement | Not verified |
| Complete end-to-end system | Partially tested |

> Simulation observations are documented separately from hardware validation. No physical-hardware test is claimed here.

---

*Additional internship tasks will be added as they are reviewed and organized.*