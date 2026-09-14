<!--
---
name: UART
class: interface
type: pinout
description: T3 Gemstone O1 UART-MAIN1 header pins and optional UART routes
url: https://docs.t3gemstone.org/en/boards/o1/peripherals/serial
pin:
  '8':
    name: UART-MAIN1 TX
    direction: output
    active: high
  '10':
    name: UART-MAIN1 RX
    direction: input
    active: high
  '11':
    name: UART-MAIN1 RTS
    direction: output
    active: low
  '36':
    name: UART-MAIN1 CTS
    direction: input
    active: low
-->
# UART - Universal Asynchronous Receiver/Transmitter

Physical Pin 8 sends and Physical Pin 10 receives. In Linux this serial port is `/dev/ttyS3`. Connect your device's receive pin to Physical Pin 8 and its send pin to Physical Pin 10, and share a ground.

Physical Pin 11 and Physical Pin 36 add flow control, RTS and CTS, for devices that need it. Most simple serial devices do not, and you can leave these two unconnected.

> **3.3 V only:** Never wire this port to an RS-232 port or a 5 V serial adapter. Both will damage the board. Use a 3.3 V USB-to-serial adapter, or a proper RS-232 level converter.

The three-pin connector on the board itself is a separate serial port used for the boot console. It is not these pins.

> **Other uses for these pins:** Some overlays move a different serial port onto Physical Pin 7 and Physical Pin 11, which also turns Bluetooth off and takes Physical Pin 11 away from flow control. Another puts a serial port on Physical Pin 18 and Physical Pin 26, which takes Physical Pin 26 away from SPI. These four pins are also shared inside the processor with the audio interface, so a full audio setup and flow control cannot both be active. Check `/boot/uEnv.txt` and reboot before wiring one of these up.
