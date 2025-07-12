# IntelliSystem Wireless PRO Controller

> A modern Bluetooth-enabled replacement controller for the Mattel Intellivision II — powered by BlueRetro, ESP32, and open-source design.

![Hero Image](docs/controller_render.png)

---

## 🎮 Features

- BlueRetro Bluetooth connectivity (ESP32)
- Cirque GlidePoint touchpad with click-wheel
- Rubber dome numpad (12 keys)
- Cherry MX-style mechanical side triggers
- USB-C + Qi wireless charging
- Rechargeable 3.7V Li-Po battery
- Intellivision II compatible FPGA receiver

---

## 🧰 Hardware Overview

| Component        | Specs                            |
|------------------|-----------------------------------|
| MCU              | ESP32-WROOM-32U                  |
| Touchpad         | Cirque GlidePoint                |
| Battery          | 1000mAh Li-Po                    |
| Charging         | TP4056 + DW01 + BQ51013B         |
| Transmitter      | ESP32 + Lattice ICE40UP5K FPGA   |

See [docs/wiring_diagram.svg](docs/wiring_diagram.svg) and [pinout.pdf](docs/pinout.pdf) for details.

---

## 🛠️ Getting Started

### ⬇️ Download Files
- [STL Models](models/stl/)
- [PCB KiCad Projects](hardware/)
- [Firmware](firmware/)
- [FPGA Logic](firmware/receiver_fpga/verilog)

### 🧑‍🏭 Build Instructions
1. 3D print the housing
2. Assemble PCB with BOM components
3. Mount GlidePoint & switches
4. Flash firmware to ESP32 and FPGA
5. Power on — ready to pair!

---

## 🚀 Flashing Firmware

### For Controller:
```bash
cd firmware/controller
pio run --target upload
