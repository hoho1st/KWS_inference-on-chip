# KWS_inference-on-chip

We will pre-train a KWS model offline, then extract the computations related structure, activation functions and weight layers of the trained model to implement on the chip, to achieve KWS inference on chip. 

This approach prioritizes low-power, low-latency solutions, making it an ideal contender for the chipIgnite challenge. 

1 We choose a lightweight neural network model - Dialation model for KWS.
2 Train the model offline using a large dataset of audio samples with PyTorch.
3 Apply model optimization techniques: pruning and knowledge distillation to reduce the size of the model
4 Convert the model from floating-point to fixed-point representation. 

5 Extract the computational graph, weight matrices, and activation functions.
6 Map the neural network architecture to a hardware design. Use wishbone to load model parameters (weights and biases) into the neural network accelerator and manage each layer's computations.
7 Use Verilog to implement the RTL design for each component. 
8 Design the interface between the RISC-V core and neural network modules. 

9 Use simulation tools to verify the correctness of our RTL design. 
