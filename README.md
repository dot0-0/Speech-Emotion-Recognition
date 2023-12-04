# Speech-Emotion-Recognition

## Table of Contents
- [About](#about)
- [Dataset](#dataset)
- [Network Architecture](#network-architecture)
- [Results](#results)
- [Requirements](#requirements)

## About
Recent years have seen a rise in interest in HAR research due to the rapid advancement of wearable sensor technology and the widespread availability of smart devices, such as gyroscopes and accelerometers built into smartphones. The methodology we present in this study automatically extracts spatial and temporal elements from smart device sensory data for the purpose of classifying HAR data. The method used to accomplish this is a hybrid supervised learning architecture made up of an LSTM (Long Short Term Memory) and a CNN (Convolutional Neural Network).

## Dataset 

RAVDESS Dataset - [RAVDESS Dataset](https://zenodo.org/records/1188976)

## Network Architecture

The neural network architecture comprises two primary blocks.

The first block constitutes a sequence of convolutional operations, initiating with a 2D convolutional layer producing 16 output channels. This layer is followed by batch normalization for stable training, ReLU activation for introducing non-linearity, max-pooling (2x2) to downsample the feature maps, and a dropout layer with a probability of 0.3 to prevent overfitting.

The second block integrates a transformer mechanism that involves multiple TransformerEncoderLayers organized within a TransformerEncoder module. This transformer block serves to reduce the input data's dimensions before undergoing transformations across multiple layers. The resulting embeddings derived from both the convolutional and transformer blocks are concatenated to combine the distinctive features.

Subsequently, the concatenated embeddings undergo linear transformation, followed by a dropout with a probability of 0.3 to further regularize the model. Finally, a softmax activation function generates class probabilities across the specified range of emotions.

This architecture is specifically designed to fuse distinctive features extracted from convolutional and transformer-based representations, thereby facilitating the prediction of emotions based on the input data.

## Results




## Requirements

Python 3.9

Pytorch 

## References

[https://github.com/jindongwang/Deep-learning-activity-recognition.git](https://github.com/jindongwang/Deep-learning-activity-recognition.git)
