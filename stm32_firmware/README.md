# STM32 Firmware

Firmware for the STM32F411CEU6-based sensor data acquisition system.

## Features
- 12-bit ADC configuration
- ADC input on PA0 (ADC1_IN0)
- USART2 serial interface on PA2 (TX) and PA3 (RX)
- STM32CubeMX-generated peripheral initialization
- STM32CubeIDE build configuration

## Build
1. Open `Sensor_Data_Acquisition.ioc` in STM32CubeMX.
2. Generate the project code.
3. Open the project in STM32CubeIDE.
4. Build using the Debug configuration.

## Validation
The firmware currently builds successfully with zero errors and zero warnings.
Physical hardware testing has not yet been performed.
