# BikeShareNN

This repository attempts to predict daily bike rental ridership. The data comes from the [UCI Machine Learning Database](https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset).

## Building a Neural Network

In our NeuralNetwork (NN), we wil implement a forward pass through the nodes and implement backpropagation to adjust the weights accordingly. In [my_answers.py](https://github.com/NadimKawwa/BikeShareNN/blob/master/my_answers.py) we define the NeuralNetwork class, and the functions associated with it.

The picture below shows a sketch of the NN. The network has two layers, a hidden layer and an output layer. The hidden layer will use the sigmoid function for activations. The output layer has only one node and is used for the regression, the output of the node is the same as the input of the node. That is, the activation function is  f(x)=x.
A function that takes the input signal and generates an output signal, but takes into account the threshold, is called an activation function. We work through each layer of our network calculating the outputs for each neuron. All of the outputs from one layer become inputs to the neurons on the next layer. This process is called forward propagation.
We use the weights to propagate signals forward from the input to the output layers in a neural network. We use the weights to also propagate error backwards from the output back into the network to update our weights. This is called backpropagation.

![nn_shape](https://github.com/NadimKawwa/BikeShareNN/blob/master/assets/neural_network.png)


## Results

The plot below shows the loss after each epoch. Notice that the loss decreases rapidly in the beginning and then flattens out.

![nn_loss](https://github.com/NadimKawwa/BikeShareNN/blob/master/bike_loss.png)


Our prediction of the data is somewhat accurate until the period starting with December 22nd. This is a special event time and should be investigated as its own dataset. One way we can account for the lack of data in that period is to synthetically produce new datapoints just for the Christmas season. However, generally speaking the model does a good job at predicting bikeshare patterns.

![alt text](https://github.com/NadimKawwa/BikeShareNN/blob/master/assets/bike_pred.png)

