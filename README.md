# Lefty-VFO
Lefty Double Conversion Transceiver Motherboard

![Alt text](VFO_rear.jpg)

This is a 4 output VFO module for the lefty transceiver.

It uses 2 SI5351/MS5351 clock generator chips. 

There is a 4 channel PCA9546 I2C multiplexer on the board which is used to switch between the two SI5351's since they have a fixed device address.

Each SI5351 is driven from a common 26 MHz TCXO source using 74LVC1G04's as a buffer.

The SI5351's have dedicated ME6211 3.3V regulators to reduce cross coupling of spurs on the 3.3v power rails.

The VFO board used a Weact "Black Pill" STM32 MPU module. This module has 512kB of flash and 128kB of ram.

The display mounts on the front of the board using a 20 pin female socket header. The display used is a 3.3V 12864 monochrome display with SPI bus capability.

The vfo board is powered from 9-15V and uses a 12V to 5V switching power supply module with input PI filter to reduce the noise generated from the switcher module.

There is one 8 pin JST XH connector supplies 12V power and provides access to the I2C bus coming from one of the PCA9546 outputs.

The vfo board supports an optional 4x4 keypad, and an optical encoder.

There are 2 pin connector for the fan output. 

There are 2 pin connectors for the ptt, tune, and s-meter inputs.

There is a 6 pin connector for the UART in the Black pill.

There is an I2C EEPROM on the board to facilitate storing VFO configuration settings

The PCB design was done with KiCAD 6.0. The BOM files are in .csv format and are included in the top level directory. There is a combined BOM, and separate top and bottom SMT BOM's.

The firmware for the VFO is in a separate project located [here] (https://github.com/hwstar/FW_VFO_STM32_BLACK_PILL_ST7920) 

The gerber files are in the directory VFO_Rev_X2_Gerbers.







