# Geosteering CSV data dictionary

One row per measured-depth sample. Header names are case-insensitive; required names are `md`, `tvdss`, `top`, and `base`. Optional names are `gr`, `phi`, `rhob`, `rt`, `rop`, `inc`, and `azi`.

| Column | Required | Units/convention | Meaning |
|---|---:|---|---|
| `md` | Yes | m, ascending after internal sort | Measured depth along well |
| `tvdss` | Yes | m, negative downward | Trajectory true vertical depth subsea |
| `top` | Yes | m, negative downward | Target top at sample MD (shallower boundary) |
| `base` | Yes | m, negative downward | Target base at sample MD (deeper boundary) |
| `gr` | No | API | Gamma ray |
| `phi` | No | fraction (v/v) | Porosity; use 0.20 for 20%, not 20 |
| `rhob` | No | g/cc | Bulk density |
| `rt` | No | ohm·m | Resistivity |
| `rop` | No | source-tool units | Rate of penetration |
| `inc` | No | degrees | Inclination |
| `azi` | No | degrees | Azimuth |

Blank optional fields are allowed. CSV commas, semicolons, or tabs are supported. At least four valid rows are required. Values must share one consistent unit system and TVDSS datum. The included CSV is wholly synthetic.
