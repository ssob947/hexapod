# Exapod – Modular Six-Leg Robot

**Work in progress.**  
This repository documents the development of a fully custom hexapod robot, including mechanics, electronics, and joint calibration methods.  
Firmware will be added once actual implementation work begins.

---

## 1. Overview

Exapod is a modular six-leg robot designed from scratch, combining:

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
- First complete leg prototype successfully assembled  

### Electronics
- TDK-Lambda i7A power module  
- BTS443P high-side switches on each leg  
- TVS surge protection and dedicated power rails  

### Sensors and Calibration
- Absolute joint encoders with AGC/MAG diagnostics  
- Per-joint angle calibration (microseconds to degrees)  
- Reference linear models for each servo  

---

## 3. Repository Structure

