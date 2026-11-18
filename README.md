# STM32 Embedded Firmware Platform

[Demo video](demo.mp4)

Board - STM32 NUCLEO-G474RE

Pins: Potentiometer on PA0 (ADC1 CH1), external LED on PC3 (TIM1 CH4)

Project Summary: A potentiometer allows for changing of the LED's PWM frequency from a range from 1 to 1000Hz. The user button on the board will cause an interrupt and allow for a changing of the duty cycle through the preset brightness levels set in the brightness_levels array found in the BSP_PB_Callback function. Changes in either the duty cycle or the frequency are printed out over an UART connection through the board's USB COM port.

## Serial output

115200 baud, 8N1 over the board's USB COM port (shows up as COM3 on my machine). An example of the output can be found in the demo video attached to the repository.

## Build and run

1. Open the project in STM32CubeIDE
2. Build and flash to the board.
3. Start a serial terminal and verify the configuration matches with the Serial output section in the readme.
4. Press user button to change duty cycle and turn the potentiometer in order to change frequency.

## Roadmap

This project is still in development and the following are additions that are planned or are in progress. Order is subject to changes as project grows:

- Improved error handling
- SPI
- I2C
- DC motor control with encoder feedback and RPM measurements
- Closed-loop motor control
- FreeRTOS
- CAN / FDCAN