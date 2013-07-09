lithne-toolchain
================

lithne-toolchain
================
This repository contains files to put in your Arduino 1.0.5 directory to make it compatible with the Lithne development boards.

The Lithne boards have an atxmega256a3u as main processor and an atxmega32a4u as co-processor. 
Arduino ships with WinAVR 2008, which is too old to know about these chips. Even WinAVR2010 does not know them. 
We therefore replace the avr toolchain by the newest toolchain from Atmel. The toolchain is not included in this repo. 

This repo includes:
* xmegaduino files (modified to fix some bugs)
* the Lithne Arduino library


To make your Arduino toolchain work with the Lithne development boards, perform the following steps:

#. Install Arduino 1.0.5
#. Remove WinAVR by deleting everything in <arduino dir>/hardware/tools/avr
#. Download the Atmel AVR toolchain from http://www.atmel.com/tools/ATMELAVRTOOLCHAINFORWINDOWS.aspx
#. Install the toolchain
#. Copy the toolchain files from where you installed them, for example 'C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.2.939\avr8-gnu-toolchain', to <arduino dir>/hardware/tools/avr/
#. Download the content of this repository as a zip file with the button on the right
#. Extract the zip file to your Arduino directory
