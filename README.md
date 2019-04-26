#FPGA Oscillator Programmer
XIlinx to ADF4351 programming to 1.763GHz
##Features
- For the ADF4351 - Wideband Synthesizer with Integrated VCO
- Tested on an Digilent CMOD-35T
- Ouput is 1.736GHz at full power (3dBm?)
- Uses Xilinx SPI IP for communication
- There is no checking that programming is sucessful
 

##How to use
1. This is an Xilinx Vivado and SDK Project: You need to program the FPGA using `download.bit` and the microblaze processor using the debugging run tools
2. Connect the oscillator using the pinout below
3. Press reset and watch for lock detect to light up
	
##Other info
###Pin out
|Cmod Pin|SPI Name|Osc. Name|
|---|---|---|
|33|SCK|CLK|
|32|MOSI|DAT|
|31|SS|LE|

###ADF Registers
|Register|Value|
|---|---|
|0|0x 00 45 00 B0|
|1|0x 00 00 80 C9|
|2|0x 00 00 4E 42|
|3|0x 00 80 04 B3|
|4|0x 00 95 00 24|
|5|0x 00 58 00 05|
