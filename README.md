# 3D Volumetric Display — Mechanical CAD Files

Mechanical design files for a rotational swept-volume volumetric display based on persistence of vision (POV). All structural components were designed in SolidWorks and fabricated by FDM 3D printing (PLA, with PETG for the motor damper).

This repository accompanies the software driver at [LoryVox](https://github.com/LoryZhong/LoryVox).

## Assembly Overview

The mechanical structure is divided into three subsystems:

### Rotate Part — Core Rotating Assembly

The central rotating body that carries all on-rotor electronics. Includes the core (with Raspberry Pi 4 mounting bosses and bearing locators), plug, slip-ring cylinder (sized for the ASL9013 2-line slip ring), bottom bearing ring, GT2 pulley bore, half-disc photo-interrupter flag, and top cover.

- Upper bearing: 6015 deep-groove ball bearing (bore large enough for the Raspberry Pi to pass through during assembly)
- Lower bearing: 6804 deep-groove ball bearing (bore sized for the ASL9013 slip ring)
- Bearings are retained by interference-fit bosses — no adhesive required

![Rotate Part](images/rotate_part.png)

**Contents of `rotate-part/`:** Core, plug, slip-ring cylinder, bottom bearing ring, half-disc flag, top cover.

### Frame — LED Panel Mounting Frame

Rectangular frames that hold each HUB75E LED panel (P2.5 64x64) at the correct radial distance from the rotation axis. Carbon-fibre rods (6 mm dia.) connect the frames to the core assembly. Version 2 redesigned the rod socket diameter to 6.1 mm with clearance chamfers, allowing post-print finishing with a 6.1 mm drill bit.

![Frame](images/frame_part.png)

**Contents of `frame/`:** LED panel frame (Version 2), rod socket geometry.

### Support Part — Stationary Base and Motor Mount

The non-rotating platform that houses the power supply, motor, brush holder (AS-PL ABH6004S), and photo-interrupter sensor. Includes the sliding motor-mount bracket for GT2 belt tension adjustment and the PETG motor damper for vibration attenuation.

![Support Part](images/support_part.png)

**Contents of `support-part/`:** Stationary base, motor mount (sliding slot), motor damper (PETG), partial enclosure panels.

## Printing Notes

| Parameter | Value |
|-----------|-------|
| Material | PLA (structural parts), PETG (motor damper) |
| Layer height | 0.2 mm |
| Infill | 20–40% (structural), 100% (bearing bosses) |
| Fasteners | M4 hex-socket screws throughout |

## License

MIT
