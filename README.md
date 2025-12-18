# Exapod – Modular Six-Leg Robot

**Work in progress.**

This repository documents the development of a custom modular hexapod robot,
covering mechanics, electronics, sensing, and calibration procedures.
Firmware will be published once active development begins.

---

## Overview

Custom six-leg robot designed from scratch with focus on:
- modular mechanical design
- repeatable joint calibration
- robust power distribution
- maintainable control architecture

The target application is **object transport**, with emphasis on stability and
predictable kinematics rather than speed.

---

## Hardware Highlights

### 3D
- Aluminium laser-cut structure
- 3D-printed structural and interface parts
- Linkage-based joints where required

### Electronics & Control
- Brushless servos (GXServo QY3242BLS)
- Teensy 4.x as main controller
- Custom power distribution (TDK-Lambda i7A, BTS443P)
- TVS protection and dedicated power rails

### Sensors
- Absolute joint encoders (AS5600, MT6835)
- Microswitches for limit/reference detection
- Encoder diagnostics via AGC/MAG monitoring

---

## Calibration & Modeling

- Per-joint angle calibration using absolute encoders
- Linear servo-to-angle models used as kinematic input
- Calibration performed per leg; representative data is published
- Data used to validate inverse kinematics consistency

---

## Repository Structure (high-level)

- `mechanics/`  
  CAD models, laser-cut parts (DXF), and 3D-printable components (STEP/STL)

- `electronics/`  
  Schematics, PCB design files, and Gerber outputs

- `docs/`  
  Calibration data, measurements, test results, and development notes

- `firmware/`  
  Intentionally omitted at this stage

---

## Project Status

**Completed**
- Prototype leg mechanics and assembly
- Encoder calibration and diagnostics
- Servo linearity characterization
- Power PCB design and validation

**In Progress**
- Body frame fabrication
- Mechanical refinement of leg assemblies
- Power system stress testing

**Planned**
- Firmware development (Teensy 4.x)
- Full inverse kinematics
- Gait generation
- Six-leg integration
