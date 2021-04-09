# OLS Logic Analyzer
You can find more information [here](https://sigrok.org/wiki/Openbench_Logic_Sniffer)

## Convert the FPGA to a Logic Analyzer
- Clone the repository
- Open the project with the VHDPlus IDE
- Compile the code (you can change the development board and pins with that the inputs are connected)
- Program the FPGA (select Extras/Long-Term Programming to save the program on the FPGA)

## Use the logic analyzer
- Download PulseView [here](https://sigrok.org/wiki/Downloads)
- Install the program
- Go to the device selection and select Openbench Logic Sniffer & SUMP compatibles (ols)
- Select the COM port of the FPGA Board, search for the device and select the logic analyzer
- Try out the functions of the program and start the logic analyzer in the upper left corner
(Be aware of the selected number of samples, the frequency and the number of channels)
- When you use the 200MHz Sample clock, the seleced sample rate is the half of the actual sample rate
