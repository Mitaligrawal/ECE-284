Dual instantiation of corelet to achieve 2x throughput on 16 output channels compared to tiling.

Same input file format as Part-2, but use 16 output channels for 4-bit activations, as well. Please place those new weights, psums, and outputs in the Tile1/ directory of P1_Files/.
Note that the models/ directory is stored in misc/. 
To run the .ipynb file, it may require editing the OS path to point to that directory.

For the 4-bit activations:
Edit the 16x16 model to use an 8x16 instead.
Also edit the output calculation code and file generation to incorporate tiling on the output channels.
Alternatively, simply use File Generation 8x16 instead.

As the 2-bit activation input files are identical to Part 2, we do not duplicate the software files here.
Please refer to Part 2's software to generate the 2-bit files.
This is only for the 4-bit, 8 input channel, 16 output channel, output channel tiling input files.