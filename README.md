# Exapod – Modular Six-Leg Robot

**Work in progress.**  
This repository documents the development of a fully custom hexapod robot, including mechanics, electronics, and joint calibration methods.  
Firmware will be added once actual implementation work begins.

---

## 1. Overview

Modular six-leg robot designed from scratch, combining:

- custom mechanics (aluminium + 3D-printed parts)
- brushless servos (GXServo QY3242BLS)
- absolute encoders (AS5600 / MT6835)
- custom power distribution and protection
- detailed servo and encoder calibration pipeline

The project focuses on accuracy, modularity, and maintainability.

---

## 2. Main Features

### Mechanical
- Aluminium laser-cut frame  
- 3D-printed interfaces and housings  

### Electronics
- TDK-Lambda i7A power module  
- BTS443P high-side switches on each leg  
- TVS surge protection and dedicated power rails  

### Sensors and Calibration
- Absolute joint encoders with AGC/MAG diagnostics  
- Per-joint angle calibration
- Reference linear models for each servo  

---

## 3. Repository Structure
mechanics/
cad/ CAD models for legs and body
laser_cut_parts/ DXF files for aluminium cutting
3d_printed_parts/ STL and source files

electronics/
schematics/ Power distribution and protection
components/ Notes on key parts and testing
wiring_diagrams/ Integration notes and cabling

docs/
calibration/ Servo and encoder calibration data
measurements/ Reference values and offset tables
images/ Photos of prototypes and assemblies

firmware/
(To be added later)



Firmware is intentionally omitted at this stage; it will be published once development begins.

---

## 4. Project Status

### Completed
- IK of a simplified prototype leg  
- Mechanical and assembly prototype of one full leg with linkage system  
- Encoder accuracy and diagnostics (AGC and MAG reference)  
- Calibration procedure and linear mapping for servos and leg joints  
- Power PCB (main and leg) design, manufacturing, and assembly  

### In Progress
- Body frame fabrication  
- Mechanical refinement of legs  
- Main power PCB stress testing  

### Upcoming
- Full controller firmware (Teensy 4.1)  
- Full inverse kinematics  
- Gait generation  
- Integration of all six legs  

---

## 5. Documentation

Detailed documentation can be found under `docs/`, including:

- calibration data and tables  
- reference measurements  
- diagrams and testing notes  

---

## 6. License

This project is intended to be released under the MIT License.  
A `LICENSE` file will be added accordingly.
