# Main Power Board

Main power distribution board for Exapod.

This board converts the 4S LiPo input to an 8 V high-current bus (servo bus) and provides a 5 V rail for logic and auxiliaries. It distributes power to the six leg power modules and exposes a 5 V/GND header for external loads.

---

## Project Status

STATUS: TEST / WORK IN PROGRESS

Hardware is functional and under validation. Final current rating and thermal limits will be confirmed through load testing and thermal characterization.

---

## System Overview

Input:
- 4S LiPo battery: Gens Ace GPGEA854S60X9GT, 8500 mAh, 14.8 V nominal, 60C (4S1P)
- External protection: MIDI fuse 40 A
- Connector: XT90 input

Main conversion:
- DC/DC module: TDK-Lambda i7A12060A008V-0F1-R
- Output setpoint: 8.0 V (fixed trim)
- Enable control: i7A EN pin is controlled by the Teensy (if Teensy is off, the 8 V bus is off)

Secondary conversion:
- 5 V buck regulator fed from VIN (battery bus)

Outputs:
- 6 × XT60 connectors supplying the six leg power boards (8 V bus)
- 30-pin Dupont-style header: 15 × GND and 15 × +5 V

Protection on PCB:
- TVS diode on VIN (input side)
- TVS diode on the 8 V bus (output side)

---

## Notes on Current and Thermal Design

- The i7A module supports up to 60 A per datasheet; however, the PCB copper and connector limits define the practical continuous current.
- Main 8 V bus copper width is approximately 14 mm.
- The module temperature at idle was measured around 65 °C (consistent with datasheet expectations).
- A 30×30 mm 5 V fan will be added, oriented as recommended in the module datasheet, to improve thermal headroom under load.

Final continuous current capability will be determined after load tests and thermal measurements.

---


## Upcoming Validation

Next planned tests:
- Output ripple and noise measurement with oscilloscope (8 V bus and 5 V rail)
- Interference evaluation (switching noise coupling)
- Load testing with 3 servos (dynamic current + transients)
- Thermal behavior with and without fan
