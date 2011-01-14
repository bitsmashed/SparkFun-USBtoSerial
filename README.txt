USB to Serial firmware used on the SparkFun ATmega8U2 Breakout Board, DEV-10277.

This project is based off of the LUFA project and Arduino USB to Serial project. The firmware needs to be compiled against LUFA 100807. To do this, download the LUFA directory within the main LUFA directory into the sparkfun_USBtoSerial project along side the Projects and Bootloaders directories.

Use:
The USB to Serial Project firmware allows the Atmega8U2 to enumerate as a SparkFun COM Port, similar to the common FTDI chip. When asked for a driver, point to the sparkfun_USBtoSerial_driver.inf file.

Load code:
The sparkFun_USBtoSerial_combined.hex has both the bootloader and USB to Serial firmware. This is the hex file installed on the SparkFun Atmega8U2 Breakout. Here is the command to burn the combined hex:
Load combined hex:

STK500 -datmega8u2 -cUSB -I150kHz -e -pf -vf -ifsparkfun_USBtoSerial_combined.hex -ms -fD9FF -EF4 -lCF -LCF

Directories:
The Bootloaders directory contains the DFU bootloader firmware. 

The Projects folder contains the USB to Serial firmware using the SparkFun VID and needs to be used with the sparkfun_USBtoSerial_driver.inf driver. SparkFun paid for the VID, so please only use for development only.  
 
ATmega8U2 Hardware Config:

Fuses - HF: 0xD9, LF: 0xFF, EF:0xF4, Lock:0x0F
16MHz crystal
