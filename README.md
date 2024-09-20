# Vanishing Gradients MLP Project

This project focuses on addressing the **vanishing gradient problem** in deep neural networks (specifically, MLPs) by experimenting with various techniques to mitigate the issue. The vanishing gradient problem occurs when gradients become too small during backpropagation, preventing effective training of the network, especially in deep models with multiple hidden layers.

## Project Overview

In this project, we explore the following six methods to alleviate the vanishing gradient issue:

1. **Weight Increasing**: Adjust the weight initialization by increasing the standard deviation to prevent vanishing gradients in the network.
   
2. **Better Activation Functions**: Replace traditional sigmoid activations with ReLU or Tanh, which have better gradient flow properties.
   
3. **Better Optimizer**: Experiment with Adam optimizer instead of standard SGD, which adapts learning rates and improves gradient propagation.
   
4. **Normalize Inside Network**: Implement Batch Normalization layers within the network to maintain gradient magnitudes and stabilize the training process.
   
5. **Skip Connection**: Introduce skip connections (residual connections) that allow gradients to bypass certain layers, reducing the likelihood of vanishing.
   
6. **Train Some Layers**: Break the deep network into smaller sub-networks and train them iteratively to avoid gradient degradation over multiple layers.

## Dataset

We used the **Fashion MNIST** dataset, consisting of 60,000 training and 10,000 test grayscale images (28x28 pixels) across 10 classes. The challenge lies in building a deep MLP that efficiently classifies these images without suffering from vanishing gradients.

## Models

Three models were experimented with, each varying in the number of hidden layers (3, 5, and 7 layers). We observed a significant performance degradation in deeper models due to the vanishing gradient problem, particularly in the 5 and 7-layer models.

## Solutions Implemented

Each solution was applied to the 7-layer MLP model, which demonstrated the most severe vanishing gradient issues. The implementation of the above techniques showed varying degrees of success in mitigating the vanishing gradient problem.

## Files

- **Solution1a_WeightIncreasing.ipynb**: Code for weight initialization with a larger standard deviation.
- **Solution2_BetterActivationFunction.ipynb**: Implements better activation functions like ReLU.
- **Solution3_BetterOptimizer.ipynb**: Tests Adam optimizer to address gradient issues.
- **Solution4a_NormalizationInsideNetwork.ipynb**: Incorporates batch normalization layers.
- **Solution5_SkipConnection.ipynb**: Adds skip connections to the deep MLP model.
- **Solution6_TrainSomeLayers.ipynb**: Trains the model in smaller sub-networks to avoid gradient issues.

## Conclusion

This project highlights the challenge of training deep neural networks due to vanishing gradients and offers multiple strategies to mitigate the issue. Each method shows promise in improving gradient flow and stabilizing the training of deep models, with **Batch Normalization** and **Skip Connections** providing particularly robust results.
