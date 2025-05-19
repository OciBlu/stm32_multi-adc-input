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
ADC1 Setting
- Mode: IN0=chek , IN1=chek, IN2=check
- Scan Conversion Mode = Enable
- Continous Conversion Mode = Enable
- Rank Sampling Time = Sama
- DMA Setting : Add ADC DMA, Mode= Normal/Circular, Increment address= Memory, Data Width= Half Time.
- NVIC Setting : Global Interrupt = Chek, ADC Interrupt = Chek
System Core / NVIC Interrupt Table / ADC Global Interrupt
- Preemtion Priority = 1

## Setting Compiler
- Buka file c_cpp_properties.json
- Ubah compilerPath jadi /usr/bin/arm-none-eabi-gcc
- Sesuaikan IncludePath
- Test compile program dengan make

## Mengatasi Error core_cm3.h
- Jika ada error: core_cm3.h: No such file or directory
- Download firmware CMSIS_4 >> [**Download CMSIS_4**](https://github.com/ARM-software/CMSIS_4)
- Copy File core_cm3.h atau semua file dari CMSIS_4 "CMSIS_4/CMSIS/Include"
- Paste file yang dicopy ke "Drivers/CMSIS/Device/ST/STM32F1xx/Include"
- Test compile program dengan make
- Pastikan tidak ada error