# Alpha5: Tiling over Input Channels

To generate random new inputs, associated golden outputs, and the trained model's weights for this alpha:
- `cd software`
- run all cells in the python notebook
- move all inputs into `hardware/datafiles`. Inside this folder, there should ultimately be:
    - Tile0/
    - Tile1/
    - activation_os.txt
    - out.txt
    - out_no_relu.txt

To run this alpha:
```
cd sim
iveri filelist
irun 
```

To tweak this alpha's testbench, in core_tb.v you may modify some parameters:
- you may turn on weight-stationary and output-stationary execution with the test_ws parameter
- most other parameters are used to tweak the dimensions of the convolution. However, we do not support the ability to
  generate new inputs in different dimensions in our python notebook, and have not tested with other dimensions.


Some notes on the expected formats of input files:
- activation_os.txt is similar in nature to activation_os.txt of Part 3, except it is the activations for two tiles' worth
  of input channels. The first 72 lines of the activations are for input channel 0, whereas the next 72 lines are for
  input channel 1. The layout of each block of activations is the same as the layout described in Part 3.
- Tile0 contains the kernel values associated with the first input tile for the first 8 output channels. Similarly, Tile1
  contains the kernel values associated with the second input tile.
- weights are laid out as in part 3, as this alpha is built on it and thus passes weights from the north through the IFIFO.
