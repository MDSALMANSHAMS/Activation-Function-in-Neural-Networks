# Activation-Function-in-Neural-Networks

It is used to determine the output of neural network. An Activation Function decides whether a neuron should be activated or not. 

<img width="374" alt="AF diag" src="https://user-images.githubusercontent.com/68110323/222917357-0d2b69dd-f4a5-4a86-8008-d56d3f5a95c9.png">

The Activation Functions can be basically divided into 3 types:-
    
A). Binary Step Activation Function, B). Linear Activation Function, C). Non-linear Activation Functions


The Nonlinear Activation Functions are mainly divided on the basis of their range or curves:-

# 1. Sigmoid 

It is especially used for models where we have to predict the probability as an output.Since probability of anything exists only between the range of 0 and 1, sigmoid is the right choice.
The Sigmoid Function curve looks like a S-shape. 

<img width="365" alt="sigmoid" src="https://user-images.githubusercontent.com/68110323/222916200-dfa483d6-ffb8-4ffb-afd6-de319aa969a2.png">

The function is differentiable.That means, we can find the slope of the sigmoid curve at any two points.


# 2. Tanh 

The tanh function is mainly used for classification between two classes. The range of the tanh function is from (-1 to 1). The advantage is that the negative inputs will be mapped strongly negative and the zero inputs will be mapped near zero in the tanh graph. The function is differentiable.

<img width="446" alt="tanH" src="https://user-images.githubusercontent.com/68110323/222916600-7d6ac733-acc8-4b68-8802-a79ecc915d03.png">

 tanh is also sigmoidal (s - shaped). Both tanh and logistic sigmoid activation functions are used in feed-forward nets.
 
 
 # 3. ReLU (Rectified Linear Unit) 
 
 It is used in almost all the convolutional neural networks or deep learning. Any negative input given to the ReLU activation function turns the value into zero immediately.
 
 <img width="222" alt="Relu" src="https://user-images.githubusercontent.com/68110323/222916838-6353d381-6fbe-4bde-a28c-f851cfb76a16.png">

 Range: [0 to infinity).  f(z) is zero when z is less than zero and f(z) is equal to z when z is above or equal to zero.
 
 
 # 4. Leaky ReLU
 
 It is an attempt to solve the dying ReLU problem. The leak helps to increase the range of the ReLU function.
 
 <img width="422" alt="Leky Relu" src="https://user-images.githubusercontent.com/68110323/222917022-8a5c3ed0-65e0-4e00-9c8d-14a24e348310.png">

  The range of the Leaky ReLU is (-infinity to infinity). The value of 'a' is 0.01.
  
  
  # 5. Parametric ReLU
  
  Parametric ReLU is another variant of ReLU that aims to solve the problem of gradient’s becoming zero for the left half of the axis. This function provides the slope of the negative part of the function as an argument a. By performing backpropagation, the most appropriate value of a is learnt.
 
 <img width="387" alt="Para Relu" src="https://user-images.githubusercontent.com/68110323/222917737-d61edfc0-755e-45b5-9861-4a4f55b81a4c.png">

 Where "a" (hyperparameter) is the slope parameter for negative values. The parameterized ReLU function is used when the leaky ReLU function still fails at solving the problem of dead neurons, and the relevant information is not successfully passed to the next layer. 
 
 
# 6. Softmax

The Softmax function is described as a combination of multiple sigmoids. 
It calculates the relative probabilities. Similar to the sigmoid activation function, the SoftMax function returns the probability of each class. It is most commonly used as an activation function for the last layer of the neural network in the case of multi-class classification. 

<img width="376" alt="Probablity" src="https://user-images.githubusercontent.com/68110323/222918274-17b3c5d7-28de-4a1d-8565-881fa0bc3269.png">

Mathematically it can be represented as:

<img width="376" alt="Softmax" src="https://user-images.githubusercontent.com/68110323/222918155-e3249c15-c1af-4d5b-8abf-9e2d71e867d6.png">


# 7. Swish

Swish consistently matches or outperforms ReLU activation function on deep networks applied to various challenging domains such as image classification, machine translation etc. 

<img width="357" alt="Swish" src="https://user-images.githubusercontent.com/68110323/222918712-795d809a-265f-4622-b51c-d415b8e9ec6e.png">

This function is bounded below but unbounded above i.e. Y approaches to a constant value as X approaches negative infinity but Y approaches to infinity as X approaches infinity.

Mathematically it can be represented as: f(x)=x*sigmoid(x)


# How to choose the right Activation Function?

You need to match your activation function for your output layer based on the type of prediction problem that you are solving—specifically, the type of predicted variable.

  Few rules for choosing the activation function for your output layer based on the type of prediction problem that you are solving:
  
1. Regression:— Linear Activation Function
2. Binary Classification:— Sigmoid Activation Function
3. Multiclass Classification:— Softmax
4. Multilabel Classification:— Sigmoid
5. Convolutional Neural Network (CNN):—ReLU activation function.
6. Recurrent Neural Network:— Tanh and/or Sigmoid activation function.

Note:-

1. ReLU activation function should only be used in the hidden layers.
2. Sigmoid and Tanh functions should not be used in hidden layers as they make the model more susceptible to problems during training (due to vanishing gradients).
3. Swish function is used in neural networks having a depth greater than 40 layers.

