<!--
---
name: 5v Power
class: interface
type: pinout
description: T3 Gemstone O1 5 V header supply pins
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/introduction
pincount: 2
pin:
  '2':
  '4':
-->
# 5 V Power

Physical Pin 2 and Physical Pin 4 supply 5 V, for add-ons that need more than 3.3 V. Remember that the signal pins are still 3.3 V only - powering a board from 5 V does not mean you can send 5 V back into a GPIO pin.

This 5 V comes from a regulator on the board rather than straight from whatever you plugged in, and the board can switch it off.

> **Do not feed power in:** These pins are an output. Pushing 5 V into them fights the board's regulator and skips the protection on the board's own power input, so it is a good way to damage something.
