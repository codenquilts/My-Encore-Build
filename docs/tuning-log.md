# Tuning log

Use dated entries so new results extend the history rather than replacing it.

## 2026-08 — Motion reliability baseline

- Corrected the pulley/belt arrangement.
- Printed a CoreXY belt-tension matcher; it reproduced the stated 0.03 mm difference.
- Reduced Klipper and OrcaSlicer maximum acceleration to 3500 mm/s².
- Raised X and Y run current equally from 0.580 A to 0.700 A RMS.
- Completed the next print without another sideways displacement.
- Measured both XY motors at approximately 38 °C.
- Measured a nominal 10 mm calibration cube within approximately 0.25 mm.

## 2026-08 — Extrusion observations

- Latest Benchy completed without the previous motion shift.
- Fine web-like stringing remained at a 220 °C hot-end temperature.
- Ambient filament humidity reading was 43%; this does not establish that the filament core is dry.

## Next controlled tests

1. Print the same small stringing model at 205 °C while keeping other settings unchanged.
2. Use 0.5 mm retraction at 40 mm/s as the K1 direct-drive starting point.
3. Test 0.7 mm retraction only if the first comparison requires it.
4. Keep Z-hop disabled during the comparison unless the model requires it.
5. If fine hairs remain, dry the spool at approximately 45–50 °C for 4–6 hours and repeat.
6. Tune pressure advance after temperature, flow and retraction are stable.
7. Fit an accelerometer and tune input shaping after the mechanical baseline is final.

## Results template

| Date | Model/material | Temperature | Retraction | Acceleration | Result | Next change |
|---|---|---:|---:|---:|---|---|
| YYYY-MM-DD |  |  |  | 3500 mm/s² |  |  |

