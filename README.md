# Throttle Cougar Extended Upgrade
Throttle Cougar Extended Upgrade is upgrade from original Thrustmaster Cougar TQS which comes with Cougar Stick.

## Goal
Goal is to use Throttle Cougar indenpendetly from Cougar Stick and add number of switches and add few encoders to extend functions in simulators such as BMS and DCS. I aimed to use throttle without any additional PC software or drivers.So I decided to build it with proven MMJoy software and Arduino. I designed modifications of throttle as such to accomodate new hardware without destroying any old hardware.

## Used hardware
- Thrustmaster Cougar TQS (obviously)
- board to connect throttle and arduino
- Arduino ProMicro with chip Atmel 32u4
- 3 shift registers 74HC165
- 9 (ON)-OFF-(ON) switches
- 2 encoders with push buttons
- 1 24 wide DIP socket for Arduino (optional)
- 3 DIP sockets DIP-16 (optional)
- 3 10pin connector for extra buttons
- 1 2x8pin connector to connect board to throttle button matrix



## Hardware
Any clone is sufficient, but must have Atmel 32u4 for I/O and USB HID function
