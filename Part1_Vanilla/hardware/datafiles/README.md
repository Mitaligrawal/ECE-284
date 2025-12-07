datafiles/ — input vectors for simulation

This directory should contain the input data files used by the testbench and verification scripts for Part1_Vanilla.

Expected files (you can add the required number of each file below with appropriate suffixes):
- weight.txt        — weight values
- activation.txt    — activation/input values
- psum.txt          — expected partial-sum / golden outputs

Guidelines:
- If you provide multiple parameter sets, name them clearly (e.g. `weight_set1.txt`, `activation_set1.txt`).
- TAs may replace these files with instructor-provided vectors for grading; ensure your testbench reads files from this relative folder.
- If your testbench expects a different filename or format, document that in `Part1_Vanilla/hardware/README.md` (not here).