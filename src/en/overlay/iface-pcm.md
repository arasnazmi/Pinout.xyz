<!--
---
name: PCM
class: interface
type: pinout
description: T3 Gemstone O1 PCM/I2S-compatible header signals
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/introduction
pin:
  '12':
    name: CLK
  '35':
    name: FS
  '38':
    name: DATA0
  '40':
    name: DATA1
-->
# PCM - Pulse-code Modulation

Four pins carry digital audio, in the same positions a Raspberry Pi uses for I2S, so an audio HAT will line up physically:

| Pin | What it carries |
| --: | :-- |
| 12 | bit clock |
| 35 | frame sync |
| 38 | audio data, the input on a Pi |
| 40 | audio data, the output on a Pi |

There is one difference worth knowing. On a Pi, Physical Pin 38 is always the input and Physical Pin 40 always the output. Here either data pin can be set up as an input or an output in software, so which one is which depends on the audio configuration rather than on the wiring.

> **Physical fit is not enough:** A Raspberry Pi audio HAT plugs in, but it will only work if the T3 Gemstone software has a driver for that HAT's audio chip and the signals are set up the right way round. Check the T3 Gemstone documentation before buying one for audio.
