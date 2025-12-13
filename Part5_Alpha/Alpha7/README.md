Please move the files from the data folders (to the appropriate test_dir), according to the input file format of the Part that it is verifying for.

2-bit corresponds to Part 2, 16x16 corresponds to Alpha 4, the other two (vanilla and nij_324) correspond to Part 1.
Note that all software is simply File Generation.
For the Alpha 4 case, you can edit the File Generation variables to produce 16x8 or 8x16 input files instead.
For the Part 2 case, the 4-bit input files should be generated the same way as for Part 1 and can be grabbed from the vanilla software directory.
For the nij_324 case, the dimensions of the layer will have to be changed to correspond with an nij of 324 and an onij of 256. (16,16 instead of 4,4 in the dimensions that aren't input/output channels.)