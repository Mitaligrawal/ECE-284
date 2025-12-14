datafiles/ — input vectors for simulation

This directory should contain the input data files used by the testbench and verification scripts for Part1_Vanilla.

Expected files (you can add the required number of each file below with appropriate suffixes):
- weight_kij0.txt, weight_kij1.txt...   — weight values
- activation.txt                        — activation/input values
- psum.txt                              — expected partial-sum / golden outputs

Guidelines:
- If you provide multiple files, name them clearly (e.g. `weight_kij0.txt`, `psum_set1.txt`).
- TAs may replace these files with instructor-provided vectors for grading; ensure your testbench reads files from this relative folder.
- If your testbench expects a different filename or format, document that in `Part1_Vanilla/hardware/README.md` (not here).

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