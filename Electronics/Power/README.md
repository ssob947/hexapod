# Power Module LEG

## Interface Summary


| Item | Value |
|---|---|
| VIN | 8 V nominal (XT60) |
| VOUT | 8 V switched (BTS443P) |
| Outputs | 3× servo power (XT30) |
| PWM signals | 3× PWM (filtered) |
| Current sensing | BTS443P IS → MCU ADC |
| Protection | TVS on VIN |
| Expansion | 4-pin bridge header + free PCB area |
| Current rating | TBD (PCB copper/thermal validation required) |



Power distribution and protection module for a single Exapod leg.

This board is designed to manage power delivery, protection, and signal conditioning for one leg, keeping the system modular and scalable.

---

## Project Status

STATUS: TEST / WORK IN PROGRESS

This PCB revision is currently under validation.  
During this phase, differences between the uploaded Gerber files and the PCB pictures may occur.

---

## Overview

The Power Module LEG provides:

- regulated power distribution to a single leg  
- controlled power switching  
- current monitoring  
- PWM signal routing and filtering  
- transient protection on the main supply input  

The electrical schematic is considered functionally correct.  
The PCB layout is still under refinement and validation.

---

## Functional Description

### Power Switching and Protection

- The board integrates a **BTS443P smart high-side switch**
- Power-up is controlled by the main MCU (Teensy)
- The switch is enabled during MCU startup to allow controlled leg activation
- The integrated **current sense (IS pin)** is routed to the MCU for:
  - real-time current monitoring
  - software-based cutoff in case of abnormal or excessive current consumption

---

### Servo Power and Signals

- Power is distributed to **three servos per leg**
- PWM control signals for the three servos are:
  - routed through the board
  - filtered to reduce noise and improve signal integrity
- Servo supply and control are handled locally to minimize wiring complexity

---

### Expandability

- Additional free PCB area is intentionally left available
- This space can be used for future features, sensing, or revisions without redesigning the entire board

---

## Validation Status

The following aspects are still under verification:

- buck regulator stability and compensation  
- voltage stability under dynamic load  
- noise and ripple behavior  
- current sensing accuracy and cutoff logic 
