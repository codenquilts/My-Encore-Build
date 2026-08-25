# OrcaSlicer profile notes

## Confirmed machine baseline

- Build area: 120 × 120 mm.
- Nozzle: 0.4 mm.
- Filament: 1.75 mm.
- Slicer acceleration should agree with the 3500 mm/s² Klipper limit.
- Extruder: Creality K1 direct drive.

## PLA tuning starting points

- The recorded 220 °C Benchy showed fine web-like stringing.
- Repeat the same model at 205 °C before changing several variables together.
- Begin direct-drive retraction testing at 0.5 mm and 40 mm/s.
- Try 0.7 mm only if the first comparison shows it is needed.
- Keep Z-hop off for the controlled comparison unless required by the model.

## Export checklist

Before adding an OrcaSlicer profile export:

- Remove printer-network details and other machine-local information.
- Record the OrcaSlicer version.
- State the filament brand/type used for validated results.
- Separate machine limits from filament-specific temperature, flow and cooling values.

