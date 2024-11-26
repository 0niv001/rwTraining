First part of a neuron is always a linear function of its inputs.

A neuron with n inputs, has n + 1 weights.

The linear function is followed by an activation function, so that neural network can represent non-linear functions.

Different activation functions:

1. Hard threshold: 1 when positive or 0
2. Logistic function: makes neuron the same as logistic regression function.
3. Rectifier: 0 when negative, otherwise it passes through input value
    - Rectified Linear Unit - ReLU
        

Neural network model is defined by the set of neurons, choice of activation function and the connection between neurons.

Model gives an hypothesis space. To choose a hypothesis we need to find a value for the weights of each neuron during training.

Limitations of single layer NNs are similar to the ones of logistic regression.

Each neuron acts independently, and we cannot represent XOR function on two outputs.

To solve the issue we need to add a hidden layer, making it a multilayered network that can represent complex functions.

### Multilayered network

Potentially less efficient to evaluate, and tend to have more weights than single layer network.

Method for training neural networks:

- Error is defined by an equation, which measures inaccuracies of the neural network on the training data set.
- Start with random values for weights, that are then tweaked to reduce error - Gradient descnet.