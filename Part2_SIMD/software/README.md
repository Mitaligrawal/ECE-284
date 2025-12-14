Part2_SIMD software folder

Place software artifacts here (notebooks, trained model files, scripts):
- `VGG16_Quantization_Aware_Training.ipynb` (include 2-bit activation and 4-bit weight variants)
- `VGG16_Quantization_Aware_Training.pdf`
- `misc/` for helper scripts and data processing utilities

- Include instructions to reproduce results (dependencies, commands) if non-standard.

The default testbench should cover both 2-bit and 4-bit modes without recompilation.

Please separate input files into two directories in Part-2. P1_Files should have activation.txt as well as one directories - Tile0. In the Tile directory, please list the outputs (in 8 col by len_onij format) in out.txt, as well as the psum_[kij].txt files and weight_[kij].txt files. These should be for the 8x8 version.

P2_Files should have the same structure, but instead of the regular 8x8 setup, the weights must be in the form of row14col0,row12col0,...,row0col0 on one line, followed by row15col0,row13col0,...,row1col0 on the next, repeated for every column. These should be for the 16x16 version with 2-bit activations. The activations should be in the form of row15time0,row14time0,...,row0time0 on one line followed by time1 on another line.
The psum and output files should have approximately the same structure as in Part 1.

Note that the models/ directory is stored in misc/. 
To run the .ipynb file, it may require editing the OS path to point to that directory.
The P1_Files should be generated the same way as for Part 1.

Please note that as the 4-bit case is exactly the same as Part 1, we simply reused the Part 1 software to pull a 4-bit layer.
The Part 1 software is not duplicated in this software directory. Please refer back to Part 1's software directory for the 4-bit case.
This software directory only generates input files for the 2-bit activation case.