<!--
---
name: I2C
class: interface
type: pinout
description: T3 Gemstone O1 I2C-MCU0 and shared I2C-WKUP0 header pins
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/i2c
pin:
  '3':
    name: I2C-MCU0 SDA
    direction: both
    active: high
  '5':
    name: I2C-MCU0 SCL
    direction: both
    active: high
  '27':
    name: I2C-WKUP0 SDA
    direction: both
    active: high
  '28':
    name: I2C-WKUP0 SCL
    direction: both
    active: high
-->
# I2C - Inter-Integrated Circuit

Physical Pin 3 (data) and Physical Pin 5 (clock) are the I2C bus for your own devices. Nothing else on the board uses it, so the whole bus is yours. The pull-up resistors an I2C bus needs are already fitted on the board, so you do not have to add any.

Different software images number the bus differently, so it can show up as `/dev/i2c-1` or `/dev/i2c-2`. Run `ls /dev/i2c-*` to see which buses exist, then `i2cdetect` on one to see what is connected.

> **Before you connect anything:** Use 3.3 V devices only. Give every device on the bus a different address, or they will fight each other. If you do add pull-up resistors, remember the board already has its own.

## Pins 27 and 28 are a shared bus

These two pins are a second, working I2C bus, with its pull-up resistors fitted just like the first one. The difference is that you are not alone on it: the chip that manages the board's power, the real-time clock and a small memory chip are already connected to it. On a Raspberry Pi this is also where a HAT keeps its identification chip, and a HAT that expects that will find it here.

So you can use these pins - you just have to share. Before choosing a device, run `i2cdetect` on this bus to see which addresses are already taken, and pick one that does not clash. Whether the bus appears as a `/dev/i2c-*` device at all depends on your software image, so check first.

> **Take more care here than on pins 3 and 5:** The power-management chip is on this bus, so a short, a wrong voltage or a device that jams the bus can take the whole board down rather than just your accessory. Do not reconfigure the devices that are already there. For everyday sensors and add-ons, Physical Pin 3 and Physical Pin 5 are the easier choice, because that bus is yours alone.
