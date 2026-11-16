# Task 04 — SD Card Data Logger

**Board / environment:** VEGA ARIES v3 / Tarcin MbedO  
**Status:** **Partially tested — SD initialization mismatch**

## Objective
Write data records to a file on a MicroSD card using the SPI interface.

## Supplied implementation
The sketch initializes SD using `SD.begin(10)` and writes records to `log.txt`.

## Observed issue
- Serial Monitor reported SD initialization failure.
- The MbedO MicroSD widget simultaneously showed a 16 GB card inserted and an increasing byte count (reported observations from 102 to 408 bytes).
- This is a mismatch between the sketch's initialization result and the simulator widget. The root cause is not established.

## Recommended next steps
- Verify the SPI pin mapping and chip-select pin expected by the ARIES v3 MbedO environment.
- Confirm whether the simulator's MicroSD component is compatible with the Arduino SD library/API used by the sketch.
- Check file-open/write return values and read the file back after writing.
- Repeat with a minimal SD initialization example before restoring the full logger.

## Files
- Sketch: `Code/Task_04_SD_Card_Data_Logger.ino`
- Report: `Documentation/Task_04_Report.md`
- Test notes: `Documentation/Testing_Notes.md`
- Add original circuit screenshots to `Circuit_Screenshot/`.

**Honest result:** Simulator widget activity was observed, but successful sketch-level SD initialization and reliable file logging are not yet confirmed.
