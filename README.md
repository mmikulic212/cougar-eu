# Throttle Cougar Extended Upgrade

Hardware upgrade for ThrustMaster Cougar TQS throttle quadrant.

## Goal

Enable ThrustMaster Cougar throttle to work independently from Cougar stick, with additional switches and encoders. Uses native USB HID - no additional drivers required.

## MMJoy Firmware

This project uses [MMJoy](https://github.com/MMJoy/mmjoy_en) - open-source USB HID joystick firmware for Arduino.

- **Download**: https://github.com/MMJoy/mmjoy_en/releases
- **Wiki**: https://github.com/MMjoy/mmjoy_en/wiki

## Hardware

![Button Setup](img/cougar_button_setup.jpg)

### Required Components

| Component | Description | Example |
|-----------|-------------|---------|
| ThrustMaster Cougar TQS | Original throttle quadrant | N/A |
| Custom PCB | Interface board | Order from `order/` |
| Arduino Pro Micro | USB HID controller (ATmega 32u4) | Generic clone, 5V/16MHz |
| 3x 74HC165 | 8-bit shift register | SN74HC165N DIP-16 |
| 9x Toggle Switch | (ON)-OFF-(ON) DPDT | RS PRO 206-6978 |
| 2x Rotary Encoder | KY-040 with push button | KY-040 module |

### Optional Components

| Component | Description |
|-----------|-------------|
| 1x 24-pin DIP socket | For Arduino Pro Micro |
| 3x 16-pin DIP socket | For 74HC165 |
| 3x 10-pin connector | For additional buttons (2x5 IDC header) |
| 1x 2x8-pin connector | For throttle button matrix |
| Ribbon cable | 10-pin flat cable |

## Wiring

![Pro Micro Pinout](references/mmjoy_promicro_pinout.png)

### Assembly Images

![Internal Overview](img/assembly_internal_overview.jpg)
*Internal view showing PCB, Arduino Pro Micro, shift registers, and wiring*

![Arduino Detail](img/assembly_arduino_detail.jpg)
*Close-up of Arduino Pro Micro installed in socket with connected wires*

![Front View](img/throttle_front_view.jpg)
*Front view of completed throttle with toggle switches*

![Side View](img/throttle_side_view.jpg)
*Side view showing throttle grip and switch placement*

## PCB

![PCB](references/cougar-pcb.png)

The custom PCB can be ordered from any PCB manufacturer (JLCPCB, PCBWay, Seeed, etc.) using Gerber files in `order/` folder.

**No electrical modifications to Cougar throttle are required** - simply connect the custom PCB.

## Getting Started

1. **Order PCB** - Download Gerber files from `order/` folder
2. **Assemble** - Solder components, install Arduino and shift registers in sockets, connect to throttle
3. **Flash firmware** - Upload MMJoy to Arduino Pro Micro ([see MMJoy Wiki](https://github.com/MMjoy/mmjoy_en/wiki/Firmware-upload))
4. **Configure** - Use MMJoy configurator to set up inputs/outputs. Load configuration from `mmjoy_setup/` or modify based on your wiring
5. **Test** - Verify all buttons, encoders, and axes work correctly

## Project Structure

| Folder | Description |
|--------|-------------|
| `board/` | PCB design files (Eagle) |
| `mmjoy_setup/` | MMJoy configuration files |
| `order/` | Gerber files for PCB manufacturing |
| `references/` | Reference documentation |

## License

CC BY-NC-SA 4.0 - Non-commercial use only, share-alike
