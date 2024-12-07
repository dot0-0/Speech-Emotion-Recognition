# Speech-Emotion-Recognition

## Table of Contents
- [About](#about)
- [Dataset](#dataset)
- [Network Architecture](#network-architecture)
- [Results](#results)
- [Requirements](#requirements)

## Dataset 

RAVDESS Dataset - [RAVDESS Dataset](https://zenodo.org/records/1188976)

## Network Architecture

This architecture is designed for emotion recognition and consists of the following components:

Convolutional Block:

It processes 2D input data, likely spectrograms or images with a single channel.
The block includes multiple convolutional layers followed by batch normalization, ReLU activation, max-pooling, and dropout. Each convolutional layer captures different features from the input.
Convolutions are performed using layers with different channel sizes, 3x3 kernel sizes, padding for spatial dimensions, and ReLU activation functions. Max-pooling reduces spatial dimensions.
Transformer Block:

After convolution, a MaxPooling2D layer reduces dimensions further.
The data is reshaped to fit the transformer's required input shape (time, batch, embedding).
The nn.TransformerEncoder is used with specific parameters for layers, input dimension, attention heads, feedforward network dimension, dropout rate, and activation function.
The transformer learns relationships and dependencies within the input sequence.
Concatenation and Final Layers:

The outputs from the convolutional and transformer blocks are concatenated.
The combined representation goes through a linear layer to map it to the output dimension representing different emotions.
Dropout is applied before the final softmax activation.
The final output includes both logits and softmax probabilities for each emotion class.
Forward Function:

The input tensor goes through both the convolutional and transformer blocks.
The outputs are concatenated and passed through the linear layer with dropout, followed by a softmax activation to generate the final predictions.

## Results

<p align="center">
  <img src="https://github.com/dot0-0/Speech-Emotion-Recognition/blob/main/ConfusionMatrix.png" alt="Alt text" width="300"> <img src="https://github.com/dot0-0/Speech-Emotion-Recognition/blob/main/Correlation.png" alt="Alt text" height="217.7"> 
</p>

## Requirements

Python 3.9

Pytorch 

## References

[https://github.com/IliaZenkov/transformer-cnn-emotion-recognition](https://github.com/IliaZenkov/transformer-cnn-emotion-recognition)
