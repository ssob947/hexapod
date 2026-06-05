# LEG_logic

![LEG_logic PCB](leg_logic_pcb_v0.1.png)

Per-leg sensing and communication board used by each hexapod leg.

The board provides encoder interfaces, communication infrastructure, local diagnostics, and expansion capabilities while keeping sensing electronics physically separated from actuator power distribution.

LEG_logic is mechanically and electrically integrated with the LEG_power board through direct pin-header connections. This approach minimizes wiring, reduces susceptibility to electrical interference, and simplifies assembly, testing, and replacement of complete leg modules.

---

# Main Functions

- Absolute encoder interfaces
  - MT6835 (SPI) for the coxa joint
  - AS5600 (I2C) for the femur and tibia joints

- Differential I2C communication with the MAIN_logic board

- PWM distribution for actuator control

- Current monitoring acquisition from the LEG_power board

- Foot contact sensor interface

- Local digital and analog expansion interfaces

---

# Communication Architecture

Communication with the central controller is performed through differential I2C transceivers to improve robustness over long cable runs.

A local I2C multiplexer is used to manage encoder devices and auxiliary peripherals.

---

# Diagnostics

The board supports:

- Encoder position feedback
- Encoder health monitoring (AGC / MAG)
- Foot contact detection
- Current monitoring through BTS443P current sense outputs
- Future diagnostic and expansion sensors

---

# Design Philosophy

Each leg contains its own dedicated sensing and communication electronics.

This modular approach allows:

- Independent testing of each leg
- Simplified troubleshooting
- Easier hardware replacement
- Reduced wiring complexity
- Future subsystem upgrades without redesigning the entire robot
