When the ATmega8U2 Breakout board plugs into USB it will enumerate as a COM port. To enter bootload mode, pull PD7 low, reset board, release reset, then release PD7. If asked for a driver, point to the Flip directory. Device should now enumerate as a AT90USB82 (NOT a ATmega8U2).  Next:

-download Atmel's Flip
-open a command prompt
-cd to the project (e.g. sparkfun_USBtoSerial-v10) dicrectory
-make clean
-make
-make flip OR open FLIP and load hex file

*ATTENTION* Be sure to use the AT90USB82 as the device in the FLIP software

Unplug, replug board, it now should come up as SparkFun COM Port.
