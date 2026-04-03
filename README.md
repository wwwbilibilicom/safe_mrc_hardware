# SafeMRC Hardware

**[English](README.md) | [中文](README_CN.md)**

> High-performance PCB design for Magnetorheological Fluid (MRF) clutch and bearing lock controllers, optimized for the STM32H7 series.

[![MCU: STM32H723](https://img.shields.io/badge/MCU-STM32H723-03234B?logo=stmicroelectronics)](https://www.st.com/en/microcontrollers-microprocessors/stm32h723-733.html)
![PCB: 4-Layer](https://img.shields.io/badge/PCB-4--Layer-green)
![Design Tool: EasyEDA Pro](https://img.shields.io/badge/Design-EasyEDA_Pro-blue)
![Form Factor: Small size](https://img.shields.io/badge/Size-Compact-orange)

<p align="center">
  <img src="https://raw.githubusercontent.com/username/safe_mrc_for_DM_firmware/main/images/hardware.png" alt="SafeMRC Hardware" width="600">
</p>

## Overview

This repository contains the hardware design files for the **SafeMRC** controller. Designed to drive Magnetorheological Fluid (MRF) clutches and bearing locks, this board provides high-precision current control and high-speed communication in a compact form factor suitable for integration into robotic joints (e.g., OpenArm).

## Key Features

- **High-Performance Processing** - Powered by STM32H723 (Cortex-M7 @ 550MHz) for ultra-fast control loops.
- **Precision Coil Drive** - Integrated H-Bridge with high-frequency PWM and low-side current sensing.
- **Dual High-Speed Communication** - 
  - **RS-485:** Supports up to 4 Mbps for low-latency multi-device bus control.
  - **CAN:** Supports Classic CAN at 1 Mbps.
- **Small Form Factor** - "Small size" design optimized for limited space in robot actuators.
- **Safety Centric** - Hardware support for real-time collision detection and rapid demagnetization.

## Repository Structure

```text
circuit_design/
├── ProDoc_Small size safemrc_2026.epro2  # EasyEDA Pro Project File
└── doc/
    ├── SCH_Schematic1_1_2025-09-04.pdf    # Full Schematic PDF
    ├── overview.pdf                       # Hardware Architecture Overview
    └── STM32H723XX.pdf                    # MCU Datasheet
```

## Technical Specifications

| Parameter | Specification |
|-----------|---------------|
| **Main MCU** | STM32H723VBT6 (LQFP-100) |
| **Power Input** | 24V DC (Recommended) |
| **Control Logic** | H-Bridge (PWM Current/Voltage Control) |
| **Sensing** | High-precision Current Shunt + ADC |
| **Communication** | Isolated RS-485 & Non-isolated CAN |
| **Feedback** | Support for external encoder input |

## Related Repositories

- **Firmware:** [safe_mrc_for_DM_firmware](https://github.com/username/safe_mrc_for_DM_firmware) - Embedded C code for this board.
- **Software SDK:** [safe_mrc_device](https://github.com/username/safe_mrc_device) - C++/Python drivers for host-side control.

## Documentation

For detailed schematics and layout information, please refer to the [circuit_design/doc/](circuit_design/doc/) directory. The project can be opened and edited using [EasyEDA Pro (JLCEDA)](https://pro.lceda.cn/).

## License

This project is licensed under the [MIT License](LICENSE).

---
Developed at the University of Science and Technology of China (USTC).
