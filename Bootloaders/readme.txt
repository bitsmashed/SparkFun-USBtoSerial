Usage:

-Download Atmel's Flip
-open a command prompt
-cd into the project (e.g. \sparkfun-usbdfu-v10) directory
-make clean
-make
-grab hex and load via AVR programmer and AVRStudio
-change fuses to (for SparkFun USBtoSerial) HF: 0xD9, LF: 0xFF, EF:0xF4, Lock:0x0F
-unplug then replug board, divers are found in the Flip directories
-if correct driver is used, board should enumerate as a *AT90USB82*
-now the board is ready to bootload code over USB using the Flip software

*ATTENTION* Be sure to use the AT90USB82 as the device in the FLIP software
