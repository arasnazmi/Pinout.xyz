# T3 Gemstone O1 Pinout

## Interactive reference for the 40-pin expansion header

Gemstone Pinout documents the physical pins, compatibility GPIO numbers and default interfaces exposed by the T3-GEM-O1 development board. The header follows the familiar Raspberry Pi 40-pin physical layout, while the underlying processor, pin multiplexing and software stack are specific to the Texas Instruments AM67A platform.

## Header interfaces

The header gives you I2C, SPI, a serial port with flow control, four digital audio signals and 3.3 V GPIO, plus hardware PWM on Physical Pin 29, Physical Pin 31, Physical Pin 32 and Physical Pin 33. Some of these only work once the matching overlay is enabled in `/boot/uEnv.txt`, so check the boot configuration before wiring anything up.

## Compatible HATs and add-ons

Physical fit does not guarantee electrical or software compatibility. The [compatible boards catalogue](/boards) lists only add-ons reviewed against the T3-GEM-O1 pin assignment, voltage requirements, pin direction, device-tree configuration and Linux driver availability.

No add-on is treated as compatible until its status is shown as **Verified** or **Conditionally compatible** in that catalogue.

Compatibility states are:

* **Verified:** hardware and software operation have been confirmed.
* **Conditionally compatible:** the board can work with documented limitations or configuration.
* **Incompatible:** the board must not be used, or a required feature is unavailable.

## Authoritative resources

* [T3 Gemstone O1 documentation](https://docs.t3gemstone.org/en/boards/o1/introduction)
* [GPIO guide](https://docs.t3gemstone.org/en/boards/o1/peripherals/gpio)
* [PWM guide](https://docs.t3gemstone.org/en/boards/o1/peripherals/pwm)
* [Open hardware design files](https://github.com/t3gemstone/hardware)

The pin assignments on this site come from the official T3 Gemstone O1 schematic, revision V0.2. The [GPIO page](/pinout/gpio.html) has a table of all 40 pins.
