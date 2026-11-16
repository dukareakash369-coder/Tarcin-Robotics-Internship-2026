# Task 09 — Bluetooth Robot with Crash Override

**Official reference:** Aries Advanced Task 128  
**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Modules:** HC-05, HC-SR04, L298N  
**Status:** **Not verified in supplied MbedO runtime**

## Objective
Control a two-motor robot using Bluetooth UART commands and apply an ultrasonic safety override that blocks forward motion when an obstacle is at or below 15 cm.

## Supplied pin mapping
- L298N: ENA D9, IN1 D7, IN2 D8; ENB D17, IN3 D18, IN4 D19.
- HC-SR04: TRIG D5, ECHO D6.
- HC-05: TXD to GP21/RX2; RXD from GP20/TX2; VCC/GND to 5V/GND as recorded in the supplied report.

This custom mapping differs from the official task map; verify voltage levels, UART routing and board pin labels before physical connection.

## Reported MbedO issues
- HC-05 component/runtime reported unsupported.
- `delayMicroseconds()` and `pulseIn()` reported unsupported/implicitly declared.
- Interpreted Lite reported custom `while` loops and function calls unsupported/skipped.
- A `Serial.println(cmd)` validation issue was reported in one attempt.

## Recommended next steps
- Use a compiled runtime/API that supports the required UART, timing and sensor operations, or adapt to documented MbedO APIs.
- Verify Bluetooth UART independently before integrating motor control.
- Verify ultrasonic distance measurement independently.
- Test the 15 cm override and ensure obstacle detection always stops forward motion.
- Check HC-05 logic-level compatibility before hardware use.

## Files
- Sketch: `Code/Task_128_Bluetooth_Robot_Crash_Override.ino`
- Report: `Documentation/Task_128_Mentor_Format_Report.md`
- Add original and updated MbedO screenshots to `Circuit_Screenshot/`.

**Honest result:** Current simulator/runtime does not validate Bluetooth control or crash-override behaviour.
