# Task 06 — Dual Motor Drive

**Official reference:** Aries Advanced Task 121  
**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Status:** **Partially tested; circuit mapping warnings remain**

## Objective
Drive two DC motors independently through an L298N dual H-bridge driver.

## Supplied pin mapping
| L298N signal | Board pin |
|---|---:|
| ENA | D9 |
| IN1 | D7 |
| IN2 | D8 |
| ENB | D17 |
| IN3 | D18 |
| IN4 | D19 |

## What the supplied report says
Serial and motor widgets reportedly showed forward/reverse states. MbedO also warned that all six GPIO pins had no matching circuit wiring. The screenshot evidence therefore does not conclusively prove the motor driver connections or physical motor operation.

## Recommended next steps
- Match every GPIO to the correct L298N input and enable pin.
- Check motor supply voltage and common ground.
- Test left and right motors separately, then test both together.
- Verify forward, reverse, brake and coast states.
- Document actual observed motor-widget behaviour with screenshots.

## Files
- Sketch: `Code/Task_121_Dual_Motor_Drive.ino`
- Report: `Documentation/Task_121_Report.md`
- Add original circuit screenshots to `Circuit_Screenshot/`.

**Honest result:** Directional control states were observed; wiring validation and complete motor operation remain to be confirmed.
