# AlexNet (CIFAR-10)

This folder contains a concise, educational implementation of the AlexNet convolutional neural network adapted to the CIFAR-10 image classification dataset.

## Contents

- `alexnet_cifar10.ipynb` — runnable notebook with data loading, preprocessing, model definition, training, evaluation, and examples of predictions and visualizations.

## Quickstart

1. Install dependencies from the repository `requirements.txt`.
2. Open `alexnet_cifar10.ipynb` with Jupyter Lab/Notebook and run cells in order.

## Notes

- The notebook uses TensorFlow and Keras. CIFAR-10 is provided by `tf.keras.datasets` so no external download is required.
- For reproducible results, set a fixed random seed (the notebook includes a seed). Typical test accuracies for this model and configuration are around 70-80% after a modest number of epochs.

## History and significance

AlexNet was introduced in 2012 in the paper "ImageNet Classification with Deep Convolutional Neural Networks" by Alex Krizhevsky, Ilya Sutskever, and Geoffrey Hinton. It won the ImageNet Large Scale Visual Recognition Challenge (ILSVRC) in 2012 with a top-5 error rate of 15.3%, significantly outperforming the previous best of 26.2%. This victory demonstrated the power of deep convolutional networks trained on large datasets and sparked the modern deep learning revolution.

## Why AlexNet matters

- Architectural innovations: AlexNet introduced several key techniques that became standard in deep learning, including ReLU activations for faster training, dropout for regularization, and data augmentation to improve generalization. It also popularized the use of GPUs for training large neural networks.
- Practical impact: The success of AlexNet revitalized interest in neural networks and convolutional architectures, leading to rapid advancements in computer vision and the development of modern architectures like VGG, ResNet, and transformers.
- Educational value: AlexNet is a foundational model that illustrates the principles of deep convolutional networks, including hierarchical feature learning, the benefits of depth, and techniques for training large models effectively.

## Architecture details (original vs this notebook)

- Original AlexNet (paper): Designed for ImageNet (224×224 RGB inputs), the network consists of 5 convolutional layers followed by 3 fully connected layers, with ReLU activations, max pooling, dropout, and local response normalization. The architecture includes approximately 60 million parameters and was trained on 1.2 million images across 1000 classes.
- This notebook adapts the architecture to CIFAR-10 (32×32 RGB inputs) with a simplified version that preserves the core design principles: multiple convolutional layers with increasing filter counts, max pooling for downsampling, dropout for regularization, and fully connected layers for classification. The model is scaled down to be suitable for the smaller dataset and computational constraints.

## Why this structure is important (technical rationale)

- Convolutional layers: Learn hierarchical features from local receptive fields, with parameter sharing reducing the number of parameters and enabling efficient learning of spatial patterns.
- ReLU activations: Provide non-linearity and help mitigate the vanishing gradient problem, allowing for deeper networks to be trained effectively.
- Max pooling: Reduces spatial dimensions, lowering computational cost and providing translation invariance for better generalization.
- Dropout: Randomly deactivates neurons during training to prevent overfitting, improving robustness on unseen data.
- Deep architecture: Multiple layers allow for increasingly abstract feature representations, from edges and textures to complex object parts and whole objects.
- Parameter efficiency: While deeper than early networks like LeNet-5, AlexNet's design balances capacity with regularization techniques to achieve strong performance on challenging datasets.

## Further reading

- Alex Krizhevsky, Ilya Sutskever, Geoffrey Hinton, "ImageNet Classification with Deep Convolutional Neural Networks" (2012).
- Good introductory resources on deep convolutional networks, including modern variants with batch normalization, residual connections, and attention mechanisms, for context on how AlexNet influenced later developments.

## More information

- See the top-level `README.md` for repository guidance and contribution notes.