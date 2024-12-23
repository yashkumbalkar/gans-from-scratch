# GAN Implementation on MNIST Dataset

This repository contains an implementation of Generative Adversarial Networks (GANs) using the MNIST dataset. The goal is to generate synthetic 
handwritten digits that resemble the original MNIST data by training a generator and a discriminator in an adversarial setting.

## Overview

Generative Adversarial Networks (GANs) consist of two neural networks:-

- **Generator:** Takes random noise as input and generates synthetic images that resemble the real images.
- **Discriminator:** Takes an image (real or generated) and determines whether the image is real or fake.

Both networks are trained simultaneously in a game-theoretic framework, where the generator tries to fool the discriminator, and 
the discriminator tries to distinguish between real and fake images.
MNIST dataset, consists of 28x28 grayscale images of handwritten digits from 0 to 9.

## Architecture

1.**Generator:-**
The generator is a neural network that takes random noise as input and transforms it into a 28x28 image. The architecture is as follows:

- Input: Latent vector (random noise)
- Fully connected layer `then` BatchNorm `then` LeakyReLU
- Fully connected layer `then` BatchNorm `then` LeakyReLU
- Fully connected layer `then` BatchNorm `then` LeakyReLU
- Output: 28x28x1 image (with a tanh activation)

2.**Discriminator:-**
The discriminator is a neural network that takes an image as input and outputs a probability score indicating whether the image is real or fake. 
The architecture is as follows:

- Input: 28x28 image
- Fully connected layer `then` BatchNorm
- Fully connected layer `then` BatchNorm `then` Dropout
- Fully connected layer → Sigmoid activation

**Results:-**

After training, the GAN  able to generate realistic images that resemble the MNIST dataset. You can monitor the training process by checking the generated 
images in the `gan.gif` file.

