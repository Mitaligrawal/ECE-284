Allows configurability of activation function between ReLU and LeakyReLU. Please change relu_en and lrelu_en (turn the one that you want to use to 1) and shift (values can be from 0-3) according to what activation function you want. Also, follow Part-1 input file format.

In the software, go into the model definition and change the scaling factor according to what you intend to use for the layer. Then change the scaling factor for the calculations of out_int in the main .ipynb file.

Otherwise, run the same as Part-1, with same input file format.