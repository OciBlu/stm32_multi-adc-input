# stm32_multi-adc-input
Programing STM32F103C8T6 Multiple ADC Input

## MCU Configuration
RCC
- HSE: Crystal/Ceramic Resonator
- LSE: Disable
SYS
- Debug: Serial Wire
- Timebase Source: SysTick
UART1
- Mode: Asynchronous
- Hardware Flow Control (RS232): Disable
ADC1
- Mode: IN0=chek , IN1=chek
