# nucleo_F030R8_stepper

Tinkering with a **Big Easy Driver** stepper motor driver board using an 
STM32 **Nucleo-F030R8** board. 
 
Reads a Potentiometer to set the pulse rate for the Big Easy Driver.
The the range is 1 to approx 1000 pulses per second. Update rate is 100mS and
the current PPS rate is displayed on the ST-LINK UART. Uses TIM16 CH1 on
PA6 to generate the step pulses. The TIM16 and ADC1 drivers are hand-written.

An optical limit switch is read and also displayed for debuggin wiring.

## Requirements

 - "Nucleo-F030R9" Developement Board from [ST Microelectronics](https://www.st.com/)
 - "Big Easy Driver" stepper motor driver board from Sparkfun.com [Item # ROB-12859](https://www.sparkfun.com/products/12859)
 - Eclipse CDT with "System Workbench for STM32" from [openstm32.org](https://www.openstm32.org/)
 - Serial Port Terminal (PuTTY, TeraTerm or equivalent). 

## Setup

See the spreadsheet in the Reference folder for a visual aid. External connections to the Nucleo Board are:

### Big Easy Driver
 - Connect Connect Big Easy DIR pin to CN10 Pin 36 (PF5)
 - Connect Connect Big Easy STEP pin to CN10 Pin 34 (PC4)
 - Connect Connect Big Easy GND pin to CN10 Pin 13 (PA6) (was Pin 32 (GND))
 - Connect Connect Big Easy M3 pin to CN10 Pin 30 (PB13)
 - Connect Connect Big Easy M2 pin to CN10 Pin 28 (PB14)
 - Connect Connect Big Easy M3 pin to CN10 Pin 26 (PB15)
 - Connect Connect Big Easy ENABLE pin to CN10 Pin 24 (PB1)

### Potentiometer
 - Connect low side to CN7 Pin 8 (GND)
 - Connect high side to CN7 Pin 12 (3.3V)
 - Connect wiper to CN7 Pin 28 (PA0 / A0)
 
### Optical Limit Switch
 - Connect low side to CN7 Pin 20 (GND)
 - Connect high side to CN7 Pin 16 (3.3V)
 - Connect wiper to CN10 Pin 38 (PF4)

### ST-LINK 
 - ST-LINK serial port is set to 38,400 baud, 8 bits, no parity, 1 stop bit (38.4K, 8N1)
 
   
## Usage

The CubeMX inititialization code for TIM16 and ADC1 in main.c generates unused warnings.
They are being retained for now for reference.

 - TBD

## License:

[MIT License](../master/LICENSE.txt)