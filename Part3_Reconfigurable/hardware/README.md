# Hardware folder layout and quick run steps

Place sources in `verilog/`, data files in `datafiles/`, and the `filelist` in `sim/`.

Run steps (for reference):
```pwsh
cd Part3_Reconfigurable/hardware/sim
iveri filelist
irun
```

The default testbench should exercise all reconfigurable modes without recompilation.

Tweaking the testbench:
- You may decide whether to test weight-stationary execution before output stationary execution by setting the `test_ws`
  parameter. If it is 0, only output stationary will be tested. If it is 1, weight stationary execution will be tested
  before output stationary. They will be tested one after another, with only a reset signal in between. Weight stationary
  execution takes longer to simulate than output stationary execution due to increased amounts of validation being
  performed for weight stationary.
