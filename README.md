# OLS Logic Analyzer
You can find more information [here](https://sigrok.org/wiki/Openbench_Logic_Sniffer)

## Convert the FPGA to a Logic Analyzer
- Clone the repository
- Open the project with the VHDPlus IDE
- Compile the code (you can change the development board and pins with that the inputs are connected)
- Program the FPGA (select Extras/Long-Term Programming to save the program on the FPGA)

## Use the logic analyzer in VHDPlus IDE
- Open the Serial Monitor with Baudrate = 115200 and HEX data format
- Set trigger: send "trig 11110001, 10000001" -> Inputs 1-4 and 8 are used for trigger -> 1 and 8 has to be high and 2 to 4 low to start sampling
- Set samples: send "sam 1000, 100" -> Captures 1000 samples with 100 samples delay before trigger
- Set samplerate: send "div 10" -> With 200MHz clock -> 200MHz/10 = 20MHz samplerate
- Run: send "run" and make sure that the logic analyzer is triggered. After the data is received, a .vcd file is created that you can open. The received data will be visualized

## Use the logic analyzer
- Download PulseView [here](https://sigrok.org/wiki/Downloads)
- Install the program
- Go to the device selection and select Openbench Logic Sniffer & SUMP compatibles (ols)
- Select the COM port of the FPGA Board, search for the device and select the logic analyzer
- Try out the functions of the program and start the logic analyzer in the upper left corner
(Be aware of the selected number of samples, the frequency and the number of channels)
- When you use the 200MHz Sample clock, the seleced sample rate is the half of the actual sample rate
