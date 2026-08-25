# Wiring notes

This is a record of known arrangements, not a substitute for tracing and verifying the completed printer.

| Function | Known arrangement | Verification still required |
|---|---|---|
| Main controller | BTT SKR Mini E3 V3.0 on the printer's 24 V supply | Confirm fuse, earth and terminal condition |
| Host | Raspberry Pi Zero 2 W powered from an LM2596 set to 5 V | Record converter rating, fuse and wire sizes |
| MCU data | USB between Pi and SKR Mini | Check the intended USB 5 V/back-power arrangement |
| ESP32/CYD | Shares the LM2596 5 V supply | Measure voltage at the device during reset events and inspect grounding/noise |
| Side fans | Two 12 V fans from a 24-to-12 V converter | Record converter rating, fan current and switching method |
| K1 extruder | TMC2209 extruder driver at 0.650 A RMS | Record connector order, rotation and exact motor part number |

## ESP32/CYD reset investigation

The Pi has remained stable while the ESP32/CYD occasionally resets. Check:

- The 5 V rail at the ESP32 under load and during heater/fan switching.
- Voltage drop through wiring and connectors.
- LM2596 thermal condition and current headroom.
- Ground continuity and noisy routing near motor/heater wiring.
- Local decoupling near the ESP32/CYD.

Add a labelled wiring photograph or diagram before making the repository public.

