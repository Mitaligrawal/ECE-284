Hardware folder layout and quick run steps

This folder contains three subfolders:
- `verilog/` : place all HDL source files here (e.g., core.v, corelet.v, mac_array.v).
- `datafiles/` : weight, activation and psum files used by the testbench.
- `sim/` : contains the `filelist` (plain text, no extension) and any simulation scripts or testbenches.

To run the automated checks (TAs will do):
```pwsh
cd Part1_Vanilla/hardware/sim
iveri filelist
irun
```

Notes:
- `filelist` must list relative paths to the sources in `../verilog/`.
- Do not include absolute paths.

Please alter row, column, len_nij, len_onij, o_ni_dim, and a_pad_ni_dim parameters in core_tb.v according to the test input used. (They are used to calculate nij’ in the testbench). This applies to all parts below, including alphas.

Activations should be stored in activations.txt in the Part-1 directory.

Weights are in the form weight_[kij].txt, where [kij] is substituted by kij value.

PSUMs (used for intermediate verification) are in the form psum_[kij].txt, where [kij] is substituted by kij value.

Outputs are in out.txt.

