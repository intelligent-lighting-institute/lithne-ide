lithne-toolchain
================
This repository contains files to put in your Arduino 1.0.5 directory to make it compatible with the Lithne development boards.

The Lithne boards have an atxmega256a3u as main processor and an atxmega32a4u as co-processor. 
Arduino ships with WinAVR 2008, which is too old to know about these chips. Even WinAVR2010 does not know them. 
We therefore replace the avr toolchain by the newest toolchain from Atmel. The toolchain is not included in this repo. 

This repo includes:
* xmegaduino files (modified to fix some bugs)
	* Modified boards.txt that includes Lithne board
	* pins_arduino.h and serial_init.cpp for Lithne
* the Lithne Arduino library

The main processor (atxmega256a3u) should be programmed with a custom bootloader, which can be found here: [https://github.com/elcojacobs/lithne-xboot]

To make your Arduino toolchain work with the Lithne development boards, perform the following steps:

1. Install Arduino 1.0.5
2. Remove WinAVR by deleting everything in \[Arduino dir\]/hardware/tools/avr
3. Download the Atmel AVR toolchain from [http://www.atmel.com/tools/ATMELAVRTOOLCHAINFORWINDOWS.aspx]
4. Install the toolchain
5. Copy the toolchain files from where you installed them, for example 'C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.2.939\avr8-gnu-toolchain', \[Arduino dir\]/hardware/tools/avr/
6. Download the content of this repository as a zip file with the button on the right
7. Extract the zip file to your Arduino directory
