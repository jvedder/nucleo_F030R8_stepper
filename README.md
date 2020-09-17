# nucleo_F030R8_stepper

Tinkering with a **Big Easy Driver** stepper motor driver board using an 
 STM32 **Nucleo-F030R8** board. 
 
Initially using a GPIO for stepping, but may later change to a timer.  Copied the
TIM16 config code from another project for now. Also may use a poteniometer wired
to PA0 = ADC1_IN0. Copied the ADC1 code from another project for now. The TIM16
and ADC1 drivers are hand-written (and include the CubeMX HAL code for reference).
 
## Requirements

 - "Nucleo-F030R9" Developement Board from [ST Microelectronics](https://www.st.com/)
 - "Big Easy Driver" stepper motor driver board from Sparkfun [Item # ROB-12859](https://www.sparkfun.com/products/12859)
 - Eclipse CDT with "System Workbench for STM32" from [openstm32.org](https://www.openstm32.org/)
 - Serial Port Terminal (PuTTY, TeraTerm or equivalent). 

## Setup

### Big Easy Driver
 - Connect Connect Big Easy DIR pin to CN10 Pin 36 (PF5)
 - Connect Connect Big Easy STEP pin to CN10 Pin 34 (PC4)
 - Connect Connect Big Easy STEP pin to CN10 Pin 32 (GND)
 - Connect Connect Big Easy M3 pin to CN10 Pin 30 (PB13)
 - Connect Connect Big Easy M2 pin to CN10 Pin 28 (PB14)
 - Connect Connect Big Easy M3 pin to CN20 Pin 26 (PB15)
 - Connect Connect Big Easy ENABLE pin to CN20 Pin 24 (PB1)

### Potentiometer
 - Connect low side to CN7 Pin 8 (GND)
 - Connect high side to CN7 Pin 12 (3.3V)
 - Connect wiper to CN7 Pin 28 (PA0 / A0)
 
### ST-LINK 
 - ST-LINK serial port is set to 8400 baud, 8 bits, no parity, 1 stop (38400, 8N1)
 
   
## Usage

 - TBD

## License:

[MIT License](../master/LICENSE.txt)