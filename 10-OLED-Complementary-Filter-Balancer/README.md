# Task 10 — OLED Complementary Filter Balancer

**Official reference:** Aries Advanced Task 155  
**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Sensors/display:** MPU-6050 and SSD1306 OLED  
**Status:** **Not verified / incomplete**

## Objective
Read accelerometer and gyroscope data from an MPU-6050, combine the estimates using a complementary filter, and display the estimated tilt angle on an SSD1306 OLED.

## Intended filter
`filteredAngle = alpha * (previousAngle + gyroRate * dt) + (1 - alpha) * accelAngle`

The supplied report records alpha = 0.96. Accelerometer tilt is estimated from gravity; gyroscope angular rate is integrated and can drift. The filter blends both estimates.

## Supplied I²C wiring
Both devices share the I²C bus:
- SDA0 / GP17
- SCL0 / GP16
- VCC to 3V3 and GND to common GND

## Reported MbedO issues
- Parser error around `mpu.getEvent(&accel, &gyro, &temp);`.
- Runtime message: no IMU data connected; simulated motion values used.
- OLED widget displayed an MbedO system screen, which is not proof that the sketch rendered the filter output.

## Recommended next steps
- Confirm support for the Adafruit MPU6050/Sensor APIs in the selected runtime.
- Use the simulator's documented IMU API or a compatible compiled runtime.
- Verify changing raw accelerometer/gyro readings first.
- Then verify the complementary-filter output and OLED display update while rotating the sensor.

## Files
- Sketch: `Code/Task_155_OLED_Complementary_Filter.ino`
- Report: `Documentation/Task_155_Mentor_Format_Report.md`
- Add original circuit/parser screenshots to `Circuit_Screenshot/`.

**Honest result:** IMU readings, filter calculation and OLED application output have not been validated.
