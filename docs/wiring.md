# Wiring notes

This is a record of known arrangements, not a substitute for tracing and verifying the completed printer.

| Function | Known arrangement | Verification still required |
|---|---|---|
| Main controller | BTT SKR Mini E3 V3.0 on the printer's 24 V supply |  |
| Host | Raspberry Pi Zero 2 W powered from an LM2596 set to 5 V |  |
| MCU data | USB between Pi and SKR Mini |  |
| ESP32/CYD | Shares the LM2596 5 V supply |  |
| Side fans | Two 12 V fans from a 24-to-12 V converter |  |
| K1 extruder | TMC2209 extruder driver at 0.650 A RMS |  |

## ESP32/CYD reset investigation

The Pi has remained stable while the ESP32/CYD occasionally resets. Check:

- Added local 220 mfd cap near the ESP32/CYD, helped at lot with resets.



