# Neural Network 
An artificial neural network is a network of neurons. Neurons in a neural network are arranged in layers. The first and the last layer are called the input and output layers. Input layers have as many neurons as the number of attributes in the data set and the output layer has as many neurons as the number of classes of the target variable (for a classification problem). For a regression problem, the number of neurons in the output layer would be 1 (a numeric variable).
A large neural networks can potentially have extremely complex structures, certain assumptions are made to simplify the way information flows in them:

- Neurons are arranged in layers and the layers are arranged sequentially.
- Neurons within the same layer do not interact with each other.
- All the inputs enter the network through the input layer and all the outputs go out of the network through the output layer.
- Neurons in consecutive layers are densely connected, i.e. all neurons in layer l are connected to all neurons in layer l+1.
- Every interconnection in the neural network has a weight associated with it, and every neuron has a bias associated with it.
- All neurons in a particular layer use the same activation function.

Neural networks are trained on weights and biases. During training, the neural network learning algorithm fits various models to the training data and selects the best model for prediction. The learning algorithm is trained with a fixed set of hyperparameters - the network structure (number of layers, number of neurons in the input, hidden and output layers etc.). It is trained on the weights and the biases, which are the parameters of the network.
 
## Feed forward propagation-A simple neural network

![Exmaple](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/network.png)