# LeNet-5 (MNIST)

This folder contains a concise, educational implementation of the LeNet-5 convolutional neural network adapted to the MNIST handwritten digits dataset.

Contents

- `lenet5_mnist.ipynb` — runnable notebook with data loading, preprocessing, model definition, training, evaluation, and examples of predictions and visualizations.

Quickstart

1. Install dependencies from the repository `requirements.txt`.
2. Open `lenet5_mnist.ipynb` with Jupyter Lab/Notebook and run cells in order.

Notes

- The notebook uses TensorFlow and Keras. MNIST is provided by `tf.keras.datasets` so no external download is required.
- For reproducible results, set a fixed random seed (the notebook includes a seed). Typical test accuracies for this model and configuration are in the high 90s after a modest number of epochs.

History and significance

LeNet-5 was introduced in 1998 in the paper "Gradient-Based Learning Applied to Document Recognition" by Yann LeCun, Léon Bottou, Yoshua Bengio, and Patrick Haffner. It is one of the earliest successful convolutional neural networks (CNNs) trained end-to-end by backpropagation and demonstrated that gradient-based learning with local receptive fields, shared weights, and pooling could reliably solve real-world image recognition tasks such as handwritten digit classification.

Why LeNet-5 matters

- Architectural innovations: LeNet-5 formalized the use of convolutional layers with local receptive fields and parameter sharing, and combined them with pooling (subsampling) layers. These design choices drastically reduce the number of parameters compared to fully connected networks and exploit spatial structure in images.
- Practical impact: The architecture showed that learned hierarchical features (edges → patterns → shapes) can be trained from raw pixels, paving the way for modern deep learning and large-scale convolutional models.
- Educational value: LeNet-5 is small enough to be understood end-to-end and large enough to illustrate the key concepts of convolutional neural networks, making it ideal for learning and experimentation.

Architecture details (original vs this notebook)

- Original LeNet-5 (paper): designed for 32×32 grayscale inputs and used the following rough structure: C1 (6×5×5 conv) → S2 (2×2 subsampling) → C3 (16×5×5 conv) → S4 (2×2 subsampling) → C5 (120 units) → F6 (84 units) → Output (10).
The network employed trainable feature detectors and a cascade of feature maps to progressively extract higher-level features.
- This notebook adapts the architecture to MNIST (28×28) and uses standard Keras layers while preserving the LeNet design principles: small conv filters, pooling for downsampling, and fully connected layers for classification.

Why this structure is important (technical rationale)

- Convolutional layers: enforce locality and parameter sharing, which makes them efficient at learning local patterns (edges, corners) that are useful across spatial positions.
- Pooling/subsampling: reduces spatial resolution, lowering computational cost, and provides a degree of translation invariance, which is important for recognizing objects regardless of small shifts.
- Hierarchical feature learning: stacking conv + pooling layers produces progressively more abstract representations that the final dense layers can combine to make robust classification decisions.
- Parameter efficiency: compared with dense networks on images, convolutional architectures require far fewer parameters for the same receptive field sizes, enabling feasible training and better generalization on vision tasks.

Further reading

- Yann LeCun, Léon Bottou, Yoshua Bengio, Patrick Haffner, "Gradient-Based Learning Applied to Document Recognition" (1998).
- Good introductory resources on convolutional networks and modern variants (e.g., deep CNNs with ReLU, batch normalization, residual connections) for context on how LeNet informed later developments.

More information

- See the top-level `README.md` for repository guidance and contribution notes.
