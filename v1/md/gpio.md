<!--
---
name: GPIO
class: interface
type: pinout
description: T3 Gemstone O1 general-purpose 3.3 V GPIO pins
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/gpio
pin:
  '3':
  '5':
  '7':
  '8':
  '10':
  '11':
  '12':
  '13':
  '15':
  '16':
  '18':
  '19':
  '21':
  '22':
  '23':
  '24':
  '26':
  '27':
  '28':
  '29':
  '31':
  '32':
  '33':
  '35':
  '36':
  '37':
  '38':
  '40':
-->
# GPIO - General Purpose Input/Output

The 40-pin header on the T3-GEM-O1 gives you 3.3 V digital pins. Each one can read an input, drive an output, or be switched to a special function such as serial, SPI, I2C, audio or PWM.

To control a pin from Linux you can use the `libgpiod` tools: `gpioinfo` to list the pins, `gpioget` and `gpioset` to read and write one. Raspberry Pi's GPIO libraries will not work here. Look the pin up by its system name rather than by its number, as the numbers can change between software versions.

> **Keep it at 3.3 V:** Every pin connects straight to the processor, with nothing in between to protect it. 5 V on any pin can destroy the board. The pins are also meant for signals, not power: use a driver, transistor or relay module to run LEDs, buzzers, relays or motors, not the pin on its own.
