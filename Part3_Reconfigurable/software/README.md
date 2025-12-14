# Part3_Reconfigurable software folder

Place software artifacts here (notebooks, trained model files, scripts):
- `VGG16_Quantization_Aware_Training.ipynb` (include variants relevant to reconfigurable design)
- `ProjectFileGen.ipynb` (For an example of how to generate activation_os.txt - must add this generation to VGG16_Quantization_Aware_Training if you wish to use VGG16 to generate activation_os)
- `VGG16_Quantization_Aware_Training.pdf`
- `misc/` for helper scripts and data processing utilities

- Include instructions to reproduce results (dependencies, commands) if non-standard.

To generate the weight files as well as a random set of inputs and golden outputs, run the entire VGG16_Quantization_Aware_Training.ipynb notebook.
This will generate the files. Copy all of these files into Part3_Reconfigurable/hardware/datafiles.
The testbench will use these datafiles to perform execution. 

There are some differences in the way the data files are generated.
- `activation_os.txt` is different from the normal ordering in activation.txt. The activation_os.txt stores data in the
  following order in order to enable convolution on output-stationary execution. Each row in the below example actually
  expands to 8 rows, with each of these subrows corresponding to each of the input channels for each nij.
  ```
  nij0  nij1  nij2  nij3  nij6  nij7  nij8  nij9
  nij1  nij2  nij3  nij6  nij7  nij8  nij9  nij10
  nij2  nij3  nij6  nij7  nij8  nij9  nij10 nij11
  nij6  nij7  nij8  nij9  nij12 nij13 nij14 nij15
  nij7  nij8  nij9  nij12 nij13 nij14 nij15 nij16
  nij8  nij9  nij12 nij13 nij14 nij15 nij16 nij17
  nij12 nij13 nij14 nij15 nij18 nij19 nij20 nij21
  nij13 nij14 nij15 nij18 nij19 nij20 nij21 nij22
  nij14 nij15 nij18 nij19 nij20 nij21 nij22 nij23

  ```
  As such, `activation_os.txt` is only meant for output-stationary execution. `activation.txt`, which stores activations
  in the normal configuration, is used for weight stationary execution. The testbench `core_tb.v` already uses each file appropriately.
- psum_\*.txt is unused, as in-place accumulation is implemented in this version in both the output-stationary and input-stationary versions.

All of the above applies for the OS version.
For WS, please refer to Part 1.