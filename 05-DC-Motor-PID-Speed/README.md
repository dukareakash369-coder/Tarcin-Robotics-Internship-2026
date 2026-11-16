# Task 05 — DC Motor PID Speed Control

**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Status:** **Preliminary motor test; PID control not verified**

## Objective
Control DC motor speed using closed-loop PID: compare target speed with measured speed, calculate control error, and adjust PWM output.

## Supplied implementation status
The supplied `main.ino` is a preliminary motor direction/control test. The supplied report does not establish a complete encoder-feedback PID loop.

## Intended control architecture
- Set a target speed (setpoint).
- Read encoder pulses and estimate actual speed.
- Calculate error = setpoint − measured speed.
- Apply proportional, integral and derivative terms.
- Clamp output to the valid PWM range and drive the motor.
- Log setpoint, measured speed and controller output for tuning.

## Supplied pin mapping
- L298N ENA: D9
- IN1: D7
- IN2: D8

The report notes that the simulator showed motor-direction messages/state but warned that D7, D8 and D9 had no matching circuit wiring. Encoder feedback and PID behaviour were not verified.

## Recommended next steps
- Add a supported encoder and validate pulse counting.
- Measure speed over a known time interval.
- Implement PID with output saturation and integral anti-windup.
- Confirm PWM-capable pin and actual driver wiring.
- Tune gains gradually and plot setpoint versus measured speed.

## Files
- Sketch: `Code/main.ino`
- Progress report: `Documentation/Task_05_Progress_Report.md`
- Add circuit screenshots to `Circuit_Screenshot/`.

**Honest result:** Preliminary motor test only; no closed-loop PID performance is claimed.
