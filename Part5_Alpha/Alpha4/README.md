This folder contains the parameterized version of the vanilla model to be able to have mac arrays with sizes other than 8x8. 

The hardware directory contains all relevant files needed to compile and run simulations. To change the size of the mac array, alter the row and col parameters at the top of the testbench provided and proceed with the normal process for simulations. Also, alter the 16x16 model in the models/ directory to have as many desired input and output channels.

The software directory contains the notebooks that can be used to generate the needed files for the test bench. Place these generated files in the hardware/datafiles folder as you would for any other section. 