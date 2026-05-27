# Hexapod – Modular Six-Leg Robot

Work in progress.

This repository documents the development of a custom modular hexapod robot, including mechanics, electronics, sensing, calibration procedures, and system architecture.

Firmware is currently under active development and will be published once the control framework reaches a stable state.

---

# Overview

Custom modular hexapod robot designed from scratch with focus on:

- mechanically serviceable leg modules
- encoder-supervised motion
- repeatable per-joint calibration
- distributed electronics architecture
- robust power and safety management
- predictable kinematic behavior

The platform is designed primarily for stable object transport and long-term maintainability rather than high-speed locomotion.

---

# Hardware Architecture

## Mechanical System

- Aluminium laser-cut chassis and leg structures
- Modular leg assemblies
- 3D-printed structural interfaces
- Lever-assisted femur/tibia transmission where required

## Electronics & Power

- Teensy 4.1 real-time controller
- Distributed custom PCBs:
  - central controller board
  - dedicated power board
  - independent leg logic boards
- TDK-Lambda i7A servo power stage
- BTS443P protected high-side switching
- Hardware UVLO and fault handling
- Separate logic and servo power domains

## Sensors & Feedback

- Absolute magnetic encoders on all joints
  - AS5600 (I2C)
  - MT6835 (SPI)
- Foot contact microswitches
- Encoder health monitoring via AGC/MAG diagnostics
- Motion supervision using encoder feedback

---

# Calibration Approach

Each joint is individually calibrated using absolute encoders.

Servo response is characterized and converted into joint-space models used directly by the kinematic system.

Calibration data is used to:

- reduce inter-leg variation
- validate inverse kinematics consistency
- monitor mechanical repeatability
- compensate assembly tolerances

Representative calibration data and measurements are included in the documentation.

---

# Repository Structure

```text
3D/
    CAD models, laser-cut parts, STEP/STL files

electronics/
    Schematics, PCB layouts, manufacturing files, and hardware notes

docs/
    Calibration data, measurements, prototype images, and development notes

firmware/
    Firmware development, calibration tools, diagnostics, and control software
