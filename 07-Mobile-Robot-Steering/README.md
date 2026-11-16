# Task 07 — Mobile Robot Left/Right Steering

**Official reference:** Aries Advanced Task 122  
**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Status:** **Code and report supplied; verify wiring and motor response**

## Objective
Implement left/right steering for a differential-drive mobile robot by controlling the two motor channels.

## Supplied project
The archive contains `Task_122_Mobile_Robot_Left_Right_Steering.ino`, a mentor-format report and four supplied circuit/simulation images.

## Validation points
- Confirm motor direction truth table for both channels.
- Check that left and right turns use the intended differential motor states.
- Verify L298N enable signals and board-to-driver wiring.
- Distinguish Serial Monitor command output from actual motor-widget movement.

## Recommended next steps
- Run forward, left, right and stop commands independently.
- Capture Serial Monitor and motor-widget state for each command.
- Resolve any GPIO-to-circuit warnings before marking steering validated.

## Files
- Sketch: `Code/Task_122_Mobile_Robot_Left_Right_Steering.ino`
- Report: `Documentation/Task_122_Mentor_Format_Report.md`
- Add the supplied four screenshots to `Circuit_Screenshot/`.

**Honest result:** Preserve the supplied code/report and validate each steering state with matching circuit evidence before claiming full operation.
