# stm32f7_playground
An STM32F7 firmware capable of rebooting into the system bootloader for firmware upgrades.

At a desired moment (press of 'user' button) the firmware enters the built-in system bootloader of STM32F7. Then it is accessible, for instance, via USART using [stm32flash](https://sourceforge.net/projects/stm32flash/).
The MCU will stay in bootloader mode until asked to exit it: stm32flash -g 0 /dev/ttyUSB0.

The project is using [PlatformIO](http://platformio.org/) with [STM32Cube](http://www.st.com/en/embedded-software/stm32cube-embedded-software.html) for building and [STM32CubeMX](http://www.st.com/en/development-tools/stm32cubemx.html) for the initial configuration.
Targeting [NUCLEO-F722ZE](http://www.st.com/content/st_com/en/products/evaluation-tools/product-evaluation-tools/mcu-eval-tools/stm32-mcu-eval-tools/stm32-mcu-nucleo/nucleo-f722ze.html) board by default.
[CLion](https://www.jetbrains.com/clion/) can be used conveniently as an IDE.

Board config nucleo_f722ze.json provided as well: put it into ~/.platformio/boards/ .
