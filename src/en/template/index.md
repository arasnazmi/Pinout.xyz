# T3 Gemstone O1 Pinout

T3 Gemstone Pinout documents the physical pins, compatibility GPIO numbers and default interfaces of the T3-GEM-O1 development board. The header uses the familiar Raspberry Pi 40-pin physical layout; the processor, the pin multiplexing options and the software stack, however, are specific to the Texas Instruments AM67A platform.

## Header interfaces

The header gives you I2C, SPI, a serial port with flow control, four digital audio signals and 3.3 V GPIO, plus hardware PWM on Physical Pin 29, Physical Pin 31, Physical Pin 32 and Physical Pin 33. Some of these only work once the matching overlay is enabled in `/boot/uEnv.txt`; check the boot configuration before wiring anything up.

## Compatible HATs and add-ons

Physical fit does not mean electrical or software compatibility. The [compatible boards catalogue](/boards) lists only boards reviewed against the T3-GEM-O1 pin assignment, voltage requirements, pin directions, device-tree configuration and Linux drivers.

An add-on is not treated as compatible unless its status is shown as **Verified** or **Conditionally compatible** in the catalogue.

Compatibility states:

* **Verified:** hardware and software operation have been confirmed.
* **Conditionally compatible:** it can work with documented limitations or configuration.
* **Incompatible:** the board must not be used, or a required feature is unavailable.

## Authoritative resources

* [T3 Gemstone O1 documentation](https://docs.t3gemstone.org/en/boards/o1/introduction)
* [GPIO guide](https://docs.t3gemstone.org/en/boards/o1/peripherals/gpio)
* [PWM guide](https://docs.t3gemstone.org/en/boards/o1/peripherals/pwm)
* [Open hardware design files](https://github.com/t3gemstone/hardware)
