datafiles/ — input vectors for simulation

This directory should contain the input data files used by the testbench and verification scripts for Part2_SIMD.

Expected files (you can add the required number of each file below with appropriate suffixes):
- weight_4bit.txt   — weight values for 4-bit mode
- weight_2bit.txt   — weight values for 2-bit mode
- activation.txt    — activation/input values
- psum.txt          — expected partial-sum / golden outputs

Guidelines:
- Provide separate sets for 2-bit and 4-bit experiments where applicable.
- TAs may replace these files with instructor-provided vectors for grading; ensure your testbench reads files from this relative folder.
- If your testbench expects different filenames or formats, document that in `Part2_SIMD/hardware/README.md`.