# Custom HUB75E Adapter PCB

Custom adapter PCB for the 3D volumetric display project, **based on and modified from** the [Active-3 adapter](https://github.com/hzeller/rpi-rgb-led-matrix/tree/master/adapter/active-3) by Henner Zeller (part of the [rpi-rgb-led-matrix](https://github.com/hzeller/rpi-rgb-led-matrix) project).

## What was changed

The original Active-3 design supports up to 3 panel chains with 4x 74HCT245 ICs. This version was modified for the volumetric display rotor:

- Reduced from 3 HUB75 outputs to 2 (matching the dual-panel rotating arm)
- Reduced from 4x to 3x 74HCT245 ICs
- Reworked board outline to fit inside the 3D-printed rotor core
- Added JST-XH 3-pin socket for photo-interrupter connection
- Added JST-XH 2-pin socket for DC-DC 5V power input
- Adjusted trace routing for improved CLK signal integrity (straighter path, increased clearance)
- Corrected via dimensions: drill 0.4 mm / annular ring 1.1 mm
- Minimum trace width: 0.33 mm (widened from original)
- Board thickness: 0.8 mm (thinner than standard 1.6 mm, to reduce rotor weight)

## Files in this directory

| File | Status | Description |
|------|--------|-------------|
| `active3-rpi-hub75-adapter.kicad_pcb` | **Modified** | PCB layout with custom modifications |
| `active3-rpi-hub75-adapter.kicad_sch` | **Modified** | Schematic with custom modifications |
| `active3-rpi-hub75-adapter.kicad_pro` | From original | KiCad project file (may not reflect all changes) |
| `active3-rpi-hub75-adapter.kicad_prl` | From original | KiCad local settings |
| `active3-rpi-hub75-adapter.csv` | From original | BOM (does not reflect modified design) |
| `active3-rpi-hub75-adapter-fab.zip` | From original | Gerbers (does not reflect modified design) |
| `schematic.pdf` | From original | Schematic PDF (does not reflect modified design) |

> **Note:** Only the `.kicad_pcb` and `.kicad_sch` files reflect the actual custom design used in the project. The other files are inherited from the original Active-3 project and may not match the modified board. Refer to the schematic and PCB layout files for the as-built design.

## Original design credit

Based on the Active-3 adapter by [Henner Zeller](https://github.com/hzeller), licensed under the rpi-rgb-led-matrix project. The original design is an open-source KiCad PCB using HCT245 level shifters to interface Raspberry Pi 3.3V GPIO with 5V HUB75 panels.
