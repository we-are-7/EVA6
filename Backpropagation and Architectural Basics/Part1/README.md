# Goal
To do simple neural network training with forward and backward propagation in different learning rates (in excel)

It is a simple neural network with one hidden layer with 2 neurons (h1, h2). The data has come from input neuron layer (i1, i2). It follows same rule as explained above. The features of Neural network are given Figure 6. The detail step is given in Excel sheet attached. 

## Neural Network Architecture 

![Exmaple](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/network0.png)

## Feed forward propagation

![Exmaple](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/FFD.JPG)

The data was given (0.99 and 0.01) to neurons which has multiplied with weights (W1 –W4) of neuron (initial weight = 0.3, 0.4, -0.2, 0.7) of first layer and output has been activated using sigmoid function. The output of that activated results will multiply with weights of next layers (output neurons; W5 to W8). The final activation on that output will compared with actual output and loss will be calculated as explained previously. 

## Backward propagation 

The backward propagation means basically updating weights according to the error calculated (actual value – predicted value). The weights will be updated according to error by partial differentiation and chain of rule.  Each step explained in Figure 7. 

![Exmaple](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/network2.png)


## Learning rate experiment

The experiment is performed with different learning late. The results showed that (Figure 8). The learning rate with high values (0.2) reaches the less loss very fast manner  (Figure 8). 

![Exmaple](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/Graph.png)


# Neural Network Concepts
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

In artificial neural networks, the output from one layer is used as input to the next layer. Such networks are called feedforward neural networks. This means there are no loops in the network - information is always fed forward, never fed back.

![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/matrix_notation.JPG)

- W is for weight matrix
- x stands for input
- y is the ground truth label
- p is the probability vector of the predicted output
- h is the output of the hidden layers (inner layer) after activation
- superscript stands for layer number
- subscript stands for the index of the individual neuron


![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/math_notation2.JPG)

## Calculation of output (h1) of each neuron happens Feed forward mechanism
Feed forward algorithm for a neural network with L hidden layer: 

	 	
	h0  = x (0th  layer is data/image)
	for l in range (0, L)
  	  hl = activation (W^l . h ^l-1)
	  P^i = normalize(e^(W0. hL) )

The above algorithm performs feed forward for a single data point through the neural network
So feed forward is summarized as 

![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/math_notation3.JPG)
Activation function: can be sigmoid, ReLu, Leaky ReLu

## Backward propagation in Neural Network  

- Training task is to compute the optimal weights by minimizing some cost function.
-  The desired output (output from the last layer) minus the actual output is the cost (or the loss), and we to tune the parameters weights that total cost is minimized.
- Total Loss = L = L1+ L1+ .... (sum of the loses of individual data points ) L1= loss of first data point 
- The loss function is defined as follows:

![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/math_notation4.JPG)

The loss function is defined in terms of the network output F(xi) and the ground truth yi. Since F(xi) depends on the weights and biases, the loss, in turn, is a function of (w, b). The average loss across all data points is denoted by G(w, b) which we want to minimize.
The loss used for a multiclass classification is the Cross-Entropy loss which can written as follows: 

![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/math_notation5.JPG)

## Chain rule of differentiation 

The chain rule provides us a technique for finding the derivative of composite functions, with the number of functions that make up the composition determining how many differentiation steps are necessary. For example, if a composite function f( x) is defined as

![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/math_notation6.JPG)

## Impact of learning rate

Gradient descent is an optimisation algorithm used to find the minimum of a function. The basic idea is to use the gradient of the function to find the direction of steepest descent, i.e. the direction in which the value of the function decreases most rapidly, and move towards the minima iteratively. 

The optimisation is done using the familiar gradient descent algorithm. Recall that in gradient descent, the parameter being optimised is iterated in the direction of reducing cost according to the following rule:

Weights are updated as below formula (a =Learning rate)


	W_new=W_old- a. ?L/ ?W

## Concept of Back propagation

![Notation1](https://github.com/we-are-7/EVA6/blob/main/Backpropagation%20and%20Architectural%20Basics/Part1/Images/math_notation7.JPG)

Concept of Back propagation is weights are updated in Back propagation. Gradients are calculated in a backward direction starting from dz3. Hence, we'll calculate the gradients in the following sequence. z= input to neuron after multiplying with weights, h = Output after activation, p =probability, w= weights
