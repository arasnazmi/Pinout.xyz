<!--
---
name: PWM
class: interface
type: pinout
description: T3 Gemstone O1 hardware PWM-capable header pins
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/pwm
pin:
  '29':
    name: PWM-0A
  '31':
    name: PWM-1A
  '32':
    name: PWM-0B
  '33':
    name: PWM-1B
-->
# PWM - Pulse-width Modulation

Four pins can produce PWM in hardware, which means the timing stays steady without the processor having to do the work. They come as two pairs:

| Pins | Channels |
| :-- | :-- |
| 29 and 32 | PWM-0A and PWM-0B |
| 31 and 33 | PWM-1A and PWM-1B |

The two pins in a pair share one frequency, but each can have its own duty cycle. So four independent duty cycles, on two frequencies.

You control them through `/sys/class/pwm`. They only work once the right overlay is listed in `/boot/uEnv.txt` - see the official PWM guide for the overlay names and which `pwmchip` each pair turns into. That guide also mentions PWM on a few other pins, which needs those pins to be switched away from their normal job first.

> **PWM does not power anything:** These pins put out a 3.3 V signal, and nothing more. A servo, a motor or an LED strip needs its own power supply, with the ground connected to a ground pin on the header, and a driver board or transistor in between.
