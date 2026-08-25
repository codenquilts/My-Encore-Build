# Build notes

## Project summary

This printer began as a compact Encore CoreXY build and was refined around readily available Creality motors, a BTT controller and a Raspberry Pi host. The largest practical gains came from correcting the motion hardware, converting from Bowden to direct drive, matching belt behaviour, lowering acceleration to a reliable level and raising marginal XY motor current.

## Hardware and electrical changes

| Area | Change | Observation |
|---|---|---|
| Controller | Installed BTT SKR Mini E3 V3.0 | Suitable compact Klipper controller with integrated TMC2209 drivers |
| Host | Installed Raspberry Pi Zero 2 W | Runs Klipper, Moonraker and Mainsail |
| MCU link | Changed attempted UART connection to USB | Resolved serial permission/connection trouble |
| Display | Moved TFT/CYD use away from the original UART2 arrangement | Simplified the working interface arrangement |
| Extrusion | Replaced Bowden setup with Creality K1 direct drive | Shorter filament path and improved extrusion control |
| Motion | Corrected pulley/belt arrangement and checked belt matching, increased xy driver current | Removed repeating first-layer banding and reduced rough sounds |
| Cooling | Supplied two 12 V side fans from a 24-to-12 V converter | Added cooling; MCU switching remains optional |
| Logic power | LM2596 converts 24 V to 5 V for Pi Zero 2 W and ESP32/CYD | Pi stable; ESP32 resets still require investigation |

## Motion fault and resolution

1. Early prints showed rough motion and a recurring sideways displacement, progressively shifting the model to the right.
2. Correcting the pulley/belt arrangement removed thin first-layer lines at roughly 8 mm spacing and improved smoothness.
3. A CoreXY belt-tension matcher reproduced the creator's stated 0.03 mm difference.
4. Acceleration was reduced to 3500 mm/s² in Klipper and matched in OrcaSlicer. This greatly reduced the fault, though an occasional shift remained.
5. Both XY TMC2209 run currents were found at 0.580 A RMS and raised equally to 0.700 A RMS.
6. The next print completed without another displacement. Both motors measured approximately 38 °C.

The working conclusion is that marginal XY torque caused occasional missed steps during CoreXY direction changes. The current reliable baseline combines corrected belt/pulley behaviour, 3500 mm/s² acceleration and 0.700 A RMS XY current.

## Current outcome

- Successful complete prints.
- No repeated layer displacement after the current increase.
- 10 mm calibration cube within approximately 0.25 mm.
- Motion substantially smoother than during initial commissioning.
- Fine PLA stringing remains the main visible quality issue in the latest recorded Benchy.

