<!--
---
name: SPI
class: interface
type: pinout
description: T3 Gemstone O1 SPI-MCU0 header pins
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/introduction
pincount: 5
pin:
  '19':
    name: SPI-MCU0 MOSI
    direction: output
    active: high
  '21':
    name: SPI-MCU0 MISO
    direction: input
    active: high
  '23':
    name: SPI-MCU0 SCLK
    direction: output
    active: high
  '24':
    name: SPI-MCU0 CS0
    direction: output
    active: low
  '26':
    name: SPI-MCU0 CS2
    direction: output
    active: low
-->
# SPI - Serial Peripheral Interface

SPI uses five pins: Physical Pin 19 sends data to your device, Physical Pin 21 receives data from it, and Physical Pin 23 is the clock. Physical Pin 24 and Physical Pin 26 are the two chip selects, which pick which device is being talked to. In Linux they appear as `/dev/spidev0.0` and `/dev/spidev0.2` once the matching overlay is enabled.

You can connect several devices to the same data and clock pins, as long as each one has its own chip select and stays quiet while its chip select is not active.

## The board's own sensors are on this bus

The pressure sensor and the motion sensor built into the board share these data and clock pins with you. They have their own chip selects, which are not on the header, so your device will not be confused with them.

> **What to watch for:** Use 3.3 V signals. Make sure your device stops driving the data-in pin whenever its chip select is inactive - if it keeps talking, the board's own sensor readings will be wrong, and the other way round too. Check which overlay is enabled before wiring, as the one-chip-select version only gives you Physical Pin 24.

> **Pin 26 has a second job:** It can instead be used as the receive line of an extra serial port. If you turn that on, Physical Pin 24 is your only chip select.
