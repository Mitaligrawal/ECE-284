Part1_Vanilla software folder

Place software artifacts here (notebooks, trained model files, scripts):
- `VGG16_Quantization_Aware_Training.ipynb`
- `VGG16_Quantization_Aware_Training.pdf`
- `misc/` for helper scripts and data processing utilities

- Include instructions to reproduce results (dependencies, commands) if non-standard.


Activations should be stored in activations.txt in the Part-1 directory.
Weights are in the form weight_[kij].txt, where [kij] is substituted by kij value.
PSUMs (used for intermediate verification) are in the form psum_[kij].txt, where [kij] is substituted by kij value.
Outputs are in out.txt.

For the ordering of the outputs, we used the same structure as was given in the homeworks.
For the weights, we have output_channel rows and input_channel columns. 
For activations, we have len_nij rows and input_channel columns. 
For psums, we have len_nij rows and output_channel columns.
For outputs, we have len_onij rows and output_channel columns.
Rows read right to left (0 on the right, 7 on the left).
Columns read top to bottom.
Refer to the software file generation if further elaboration needed.

Note that the models/ directory is stored in misc/. 
To run the .ipynb file, it may require editing the OS path to point to that directory.