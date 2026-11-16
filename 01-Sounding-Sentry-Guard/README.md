# Task 01 — Sounding Sentry Guard

**Official reference:** Aries Advanced Task 141  
**Board / environment:** VEGA ARIES v2 / Tarcin MbedO  
**Status:** **Partially tested**

## Objective
Build a sensor-based security alert prototype that combines motion detection and ultrasonic distance sensing, then signals an alert through a buzzer and 16×2 I²C LCD.

## Hardware and pin mapping in supplied sketch
| Part | Signal | Pin / interface |
|---|---|---|
| HC-SR04 | TRIG | D14 |
| HC-SR04 | ECHO | D15 |
| PIR | OUT | D17 |
| Buzzer | Signal | D12 |
| 16×2 LCD | I²C | I²C bus |

## Expected operation
1. PIR detects motion.
2. Ultrasonic sensor measures distance.
3. Alert logic decides whether to trigger the buzzer.
4. Status is shown through Serial Monitor and LCD.

## What the supplied evidence shows
- PIR activation produced an intruder-alert message and buzzer output HIGH.
- PIR inactive state produced a secure-status message.
- An alert message showed distance as 0 cm; this is not accepted as a verified ranging result.

## Known issue
The tested ARIES v2 browser runtime reported Arduino-style `pulseIn()` and `delayMicroseconds()` as unavailable/undefined. Therefore ultrasonic timing was not validated.

## Recommended next steps
- Replace unsupported timing calls with an API supported by the exact ARIES v2 runtime.
- Verify TRIG/ECHO wiring and sensor component support.
- Test known distances and record repeatable readings.
- Test PIR alert, buzzer and LCD independently, then perform an end-to-end run.

## Files and evidence
- Supplied sketch: `Code/sounding_sentry_guard_original.ino`
- Detailed supplied report: `Documentation/Task_01_Sounding_Sentry_Guard_Report.md`
- Add original MbedO screenshots to `Circuit_Screenshot/`.

**Honest result:** PIR alert path observed; ultrasonic distance measurement and complete system remain unverified.
