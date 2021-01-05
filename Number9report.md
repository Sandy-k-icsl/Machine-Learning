## Report for number 9

**GAN Algorithm used: DCGAN**
## Introduction
Generative Adversarial Networks (GANs) employ two deep learning architectures as adversaries – Generator and Discriminator to promote the Generator to create data that belong to a particular dataset. GANs have proven to be able to generate images that look at least superficially authentic to human eyes. For a Generator to be able to learn the mappings from a latent variable space to a particular data distribution, it is imperative for the Discriminator to be a stronger model, that is, a stronger classifier. A strong Discriminator will force the Generator to find the features relevant to the data distribution, thus, improving the Generator’s performance. Deep Convolutional GAN (DCGAN) features a deconvolutional neural network that generates data (the Generator) and a convolutional neural network model that classifies whether an input image is a fake or a real image. 

## Architecture of DCGAN
The Deconvolutional Neural Network (Generator)  is made up of 4 convolutional layers. The activation used for non-linearity is Leaky-ReLU. The last layer in the Generator uses tanh activation. The Discriminator is a Deep Convolutional Neural Network with 4 convolutional layers with Leaky-ReLU activation at each layer except for the last layer the activation used is  sigmoid to produce probabilities for classes. 

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/dcgan%20model.PNG)

## Define loss functions
-   **Discriminator loss**
    
    -   The discriminator loss function takes 2 inputs;  ** real images**,  **generated images**
    -   D_loss_real is a sigmoid cross entropy loss of the  **real images**  and an  **array of ones (since these are the real images)**
    -   D_loss_fake is a sigmoid cross entropy loss of the  **generated images**  and an  **array of zeros (since these are the fake images)**
    -   Then the D_loss is the sum of D_loss_real and the D_loss_fake
-   **Generator loss**
    -   It is a sigmoid cross entropy loss of the generated images and an  **array of ones**

## Training

-   Start by iterating over the dataset
-   The generator is given  **noise as an input**  which when passed through the generator model will output a image looking like a real image
-   The discriminator is given the  **real FASHION MNIST images as well as the generated images (from the generator)**.
-   Next, calculate the generator and the discriminator loss.
-   Then, calculate the gradients of loss with respect to both the generator and the discriminator variables (inputs) and apply those to the optimizer.
- The learning rate for the model is 0.0002 and a batch size of 100 for 30 epochs.

## Results
The figure below shows  the training results:


![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/dcgan_fashion_mnist_images/training%20results.PNG)

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/dcgan_fashion_mnist_images/FASHION_MNIST_DCGAN_train_hist.png)

## Generated image for epoch 1 and 30
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/dcgan_fashion_mnist_images/FASHION_MNIST_DCGAN_1.png)
![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/dcgan_fashion_mnist_images/FASHION_MNIST_DCGAN_30.png)


## Generated GIF of all the saved images

![enter image description here](https://github.com/SANDRAKUMI/Machine-learning-homework/blob/master/FASHION_MNIST_DCGAN_generation_animation.gif)



**By Sandra Kumi/20185122
