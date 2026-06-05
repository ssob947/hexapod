# Electronics

The electronics architecture is divided into four independent modules:

## MAIN_power

Main power distribution and protection board.

Responsibilities:
- Battery power distribution
- Servo power management
- UVLO generation
- Protection and safety functions

## MAIN_logic

Central controller board.

Responsibilities:
- Teensy 4.1 real-time control
- ESP32 communication subsystem
- I2C multiplexing
- Differential communication interfaces
- System management and diagnostics

## LEG_power

Per-leg power board.

Responsibilities:
- Servo power switching
- Current sensing
- Protection functions
- Power distribution to actuators

## LEG_logic

Per-leg sensing and communication board.

Responsibilities:
- Encoder interfaces
- Differential I2C communication
- PWM generation
- Analog and digital sensing
- Local expansion interfaces

---

Each module contains:

- Electrical schematics
- PCB image
- PCB layout view
- Manufacturing Gerber files
