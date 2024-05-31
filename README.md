# Plant Disease Recognition using Spiking Neural Network

## Introduction
This research project explores the use of Spiking Neural Networks (SNNs) for plant disease recognition, leveraging a dataset from Kaggle that consists of 1532 images classified as rusty, powdery, and healthy.

## Background
SNNs are inspired by biological neural networks, using discrete spikes for information processing, offering advantages like low power consumption and event-driven computation. Despite their potential, SNNs have been underexplored in plant disease recognition. This research aims to leverage SNNs to address limitations of current methods and enhance the precision and efficiency of disease detection systems.

## Experimental/Modeling Design
### Dataset Preprocessing
- Dataset: Plant Disease Recognition Dataset from Kaggle, with images categorized as rusty, powdery, and healthy.
- Image Resizing: Images resized to 1024 x 1024 pixels.
- Normalization: Pixel values normalized to have a mean of 0.485 and a standard deviation of 0.229.

### Model Architecture
- Convolutional Layers: Multiple layers for feature extraction.
- Pooling Layers: Max-pooling layers for downsampling.
- Fully Connected Layers: Integrate features for prediction.
- Leaky Integrate-and-Fire Neurons: Simulate biological neurons, accumulating membrane potential and emitting spikes.

### Training Procedure
- Loss Function: Combines Mean Squared Error (MSE) loss with spike-based counting metrics.
- Optimizer: Adam optimizer with a learning rate of 1e-6.
- Training Loop: Forward pass, loss computation, backpropagation, and weight updates.
- Validation: Performance evaluated on a separate validation set.

### Models Tried
- CNN: We first created a Convolutional Neural Network to have a baseline.
- SNN using Norse library: Tried to implement a SNN model using Norse Library.
- SNN using SNNTorch library: Using snntorch library with SNN and ANN, achieving a validation accuracy of 56% with a 1024x1024 input size.

## Results and Discussion
- Baseline CNN: Achieved 96% accuracy.
- SNN with ANN: Validation accuracies ranged between 35%-45%.
- SNN with CNN and ANN: Achieved 56% accuracy with a 1024x1024 input size.
- Challenges: SNN models showed potential but fell short of CNN accuracy, highlighting the need for further optimization.

## Conclusions
This research underscores the potential and limitations of SNNs in plant disease recognition. While promising, SNNs require further exploration and optimization to match the performance of traditional CNNs. Continued research can enhance the capabilities of SNNs, contributing to improved agricultural monitoring and food security.

Further Reading
For a detailed report on this research, please refer to the [full report here](Project_Report.pdf).
