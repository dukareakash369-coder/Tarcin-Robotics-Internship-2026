# Task 02 — Line Following Robot

**Official reference:** Aries Advanced Task 125  
**Board / environment:** VEGA ARIES v2 / Tarcin MbedO  
**Status:** **Partially tested; motor motion not verified**

## Objective
Use two IR line sensors to decide whether a differential-drive robot should move forward, correct left/right, or stop while following a line.

## Supplied pin mapping
| Part | Signal | Pin |
|---|---|---|
| Left IR sensor | OUT | D9 |
| Right IR sensor | OUT | D8 |
| L298N | IN1, IN2, IN3, IN4 | D14, D15, D13, D12 |

## Control concept
Read both IR sensor states, apply the line-following truth table, then set motor direction through the L298N. The correct sensor polarity depends on the actual IR modules and line/surface contrast and must be calibrated.

## Supplied evidence / issue
- Serial Monitor showed HIGH/HIGH leading to a stop state.
- MbedO reported that D12–D15 had no matching circuit wiring.
- Serial output alone does not prove that the motors physically moved.

## Recommended next steps
- Wire and verify every L298N input and motor supply.
- Confirm sensor polarity over both the line and floor.
- Record all four sensor combinations and expected motor actions.
- Test each motor independently before enabling autonomous line tracking.

## Files
- Sketch: `Code/Task_02_Line_Following_Robot.ino`
- Report: `Documentation/Task_02_Documentation.md`
- Screenshots: add to `Circuit_Screenshot/`.

**Honest result:** Sensor/decision output was observed; motor response and full line-following behaviour need verification.
