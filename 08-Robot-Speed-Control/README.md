# Task 08 — Robot Speed Control

**Official reference:** Aries Advanced Task 123  
**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Status:** **Code prepared; PWM behaviour not verified**

## Objective
Use PWM to select stop, slow, medium and full-speed motor commands while controlling direction through an L298N driver.

## Supplied control values
- 0: Stop
- 100: Slow
- 180: Medium
- 255: Full speed

## Supplied pin mapping
- ENA D9; IN1 D7; IN2 D8
- ENB D17; IN3 D18; IN4 D19

The supplied report explicitly notes this custom mapping differs from the official Task 123 mapping (ENA GPIO11, ENB GPIO10, IN1–IN4 GPIO14, GPIO15, GPIO13, GPIO12). Do not assume either mapping is correct for the current circuit without checking it.

## Supplied evidence / issues
- Six warnings reported that D7, D8, D9, D17, D18 and D19 had no matching circuit wiring.
- The screenshot's Serial Monitor showed a Task 122-style `Direction: Forward` message rather than the expected Task 123 speed-level messages.
- The screenshot therefore does not prove PWM speed changes.

## Recommended next steps
- Verify the official/custom pin mapping against the actual circuit.
- Confirm PWM support on the selected enable pins.
- Remove ENA/ENB jumpers if enable pins are driven by GPIO, where required by the driver wiring.
- Run the Task 123 sketch and capture stop/slow/medium/full-speed outputs and motor response.

## Files
- Sketch: `Code/Task_123_Robot_Speed_Control.ino`
- Report: `Documentation/Task_123_Mentor_Format_Report.md`
- Add supplied screenshot to `Circuit_Screenshot/`.

**Honest result:** PWM speed-control behaviour remains unverified.
