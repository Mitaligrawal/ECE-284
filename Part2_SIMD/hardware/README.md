Hardware folder layout and quick run steps

Place sources in `verilog/`, data files in `datafiles/`, and the `filelist` in `sim/`.

Run steps (for reference):
```pwsh
cd Part2_SIMD/hardware/sim
iveri filelist
irun
```

The default testbench should cover both 2-bit and 4-bit modes without recompilation.

Please separate input files into two directories in Part-2. P1_Files should have activation.txt as well as one directories - Tile0. In the Tile directory, please list the outputs (in 8 col by len_onij format) in out.txt, as well as the psum_[kij].txt files and weight_[kij].txt files. These should be for the 8x16 version, with tiling on the output channels and 4-bit activations.

P2_Files should have the same structure, but instead of the regular 8x8 setup, the weights must be in the form of row14col0,row12col0,...,row0col0 on one line followed by row15col0,row13col0,...,row1col0 on the next, repeated for every column. These should be for the 16x16 version with 2-bit activations. The activations should be in the form of row15time0,row14time0,...,row0time0 on one line followed by time1 on another line.

