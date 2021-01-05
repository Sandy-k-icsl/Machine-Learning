

## CNN with Tensorflow for Fashion Mnist

## Report for number 8

## Introduction
Fashion-MNIST is a data-set of Zalando's article images—consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes.

 1. **Loading of packages and Fetching of data-set**
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/data.PNG)

 2. **Categorizing and displaying of data**
 ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/classes.PNG)

 3. **Split Data-sets**

I split the original training data into training and validation. This helps to see whether we’re over-fitting on the training data and whether we should lower the learning rate and train for more epochs if validation accuracy is higher than training accuracy or stop over-training if training accuracy shift higher than the validation.

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/split.PNG)

 4. **Preprocessing of Datasets**

Data must be preprocessed before training the neural network. I preprocessed the data by performing mean subtraction and normalization.
For normalizing, scale values to a range of 0 to 1 before feeding to the neural network model. For this, cast the datatype of the image components from an integer to a float, and divide by 255.
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/norm.PNG)

#### Mean Subtraction
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/mean.PNG)

#### For the processing of the labels, I performed one hot encoding
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/labels%20encode.PNG)

 5. **Building of the CNN model**
 
 In the building of the model, I used a standard conv-net. It consists of 3 convolution layers, each followed by a max pooling layer. The output of the third max-pooling layer is flattened and fed into a fully connected hidden layer with 128 neurons `ReLU or SeLU` activation function. Finally, the output layer contains 10 neurons, with `softmax` activation function. For initializers, I used he normal initializer. I used three different regularizers: Dropout, L1 and L2. The purpose of the regularizer is to overcome the overfitting. Dropout have the rate parameter that will control how many nodes that active during the training process. L1 and L2 regularizations have a λ parameter which is directly proportional to the penalty: the larger λ the stronger penalty to find complex models and it will be more likely that the model will avoid them. For optimizers, I used Adam and Adagrad optimizers.
 ![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/Layers.PNG)
 
 7. **Reshaping of data**

Before training, data should be reshaped into three dimensions since the model is made up of three layers. NB: Reshaping of data should match the number of layers in your model.
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/reshape.PNG)

 7. **Training of the model**

First, you need to `compile` model before you can start training. I performed 10 epochs during training.

**1st Scenario**

Regularizer:  L2 with learning rate of 0.01, Optimizer: Adam, Activation: ReLU.

With the first scenario, the test accuracy was **0.8546**.
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/epochs.PNG)
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/scenario%201.PNG)


**2nd Scenario**

Regularizer: L1 with learning rate of 0.01, Optimizer: Adagrad, Activation: SeLU.

With the second scenario, the test accuracy was **0.7307.**
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/epochsl1.PNG)
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/cnn_fm_images/scenario%202.PNG)

Actual code can be found [here](https://colab.research.google.com/drive/1YwEDZMVVOsdLDFwd6NQH9x_YbipxgNAI)

**By Sandra Kumi/20185122**
