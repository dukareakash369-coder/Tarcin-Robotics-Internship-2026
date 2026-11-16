# Task 03 — Robot Wall Follower

**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Status:** **Incomplete — supplied sketch is a motor sequence test, not a complete wall follower**

## Objective
Maintain a target side-wall distance using an ultrasonic sensor and control two DC motors for differential steering.

## Supplied implementation
The provided file is `Task_03_Motor_Test_VEGA_ARIES_V3.ino`. It exercises motor direction sequences; it does not implement closed-loop wall following.

## Key concepts
- Differential-drive steering using independent left/right motor commands.
- L298N direction inputs and ENA/ENB enable signals.
- Ultrasonic trigger/echo timing and distance threshold control.
- Serial diagnostics must be paired with observed motor/sensor behaviour.

## Reported MbedO issues
- HC-SR04 component reported unsupported in the selected runtime.
- `delayMicroseconds()` and `pulseIn()` were undefined.
- Numeric `Serial.print()` was rejected in the tested browser build; report notes using formatted `printf()` instead.
- Designer save reported a schema/mapping error involving `components[0]` and unsupported `props`.
- D12–D15 had no matching circuit wiring.

## Recommended next steps
1. Resolve motor wiring and ENA/ENB enable connections.
2. Confirm a supported ultrasonic sensor component/API.
3. Implement and test distance acquisition independently.
4. Add threshold-based left/right/stop logic.
5. Verify motor response and distance feedback before claiming wall-following operation.

## Files
- Supplied sketch: `Code/Task_03_Motor_Test_VEGA_ARIES_V3.ino`
- Report: `Documentation/Task_03_Robot_Wall_Follower_Report.md`
- Add original circuit screenshot to `Circuit_Screenshot/`.

**Honest result:** Motor command sequence was observed in Serial Monitor; autonomous wall following is not complete.
