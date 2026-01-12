
# Neural Network Architectures (Educational Cookbook)

A small collection of reference implementations and interactive notebooks demonstrating classic convolutional neural network architectures and training workflows on standard datasets (MNIST, CIFAR-10). The repository is intended for learning, reproducibility, and quick experiments.

## Workflows

- Each subfolder contains a self-contained notebook that demonstrates data loading, model definition, training loop, evaluation, and simple visualizations. Notebooks are runnable end-to-end but may be adapted into scripts for production or experiments.

- If you want to reproduce experiments exactly, set random seeds and pin package versions from `requirements.txt`.

## Contributing

Contributions are welcome. Please open an issue to propose a change or submit a pull request with a clear description of the change, why it is needed, and any results or tests.

Guidelines:

- Keep notebooks readable and well-documented
- Add or update a `README.md` in any new subfolder you add
- Include small, focused commits with clear messages

## License

This project is provided under the MIT License. See the `LICENSE` file for details.


## Table of contents

- [Quickstart](#quickstart)
- [Repository structure](#repository-structure)
- [Workflows](#workflows)
- [Contributing](#contributing)
- [License](#license)

## Quickstart

Prerequisites

- Python 3.9+ (or compatible)
- pip
- Optional: GPU with CUDA if you want to train faster

Basic setup

1. Create and activate a virtual environment (recommended):

```bash
python -m venv .venv
source .venv/bin/activate  # macOS / Linux
.venv\Scripts\activate     # Windows
```

2. Install required packages:

```bash
pip install -r requirements.txt
```

3. Open a notebook server and run one of the examples:

```bash
jupyter lab  # or jupyter notebook
```

Open any notebook (for example, `lenet/lenet5_mnist.ipynb`) and follow the cells.

## Repository structure

```
neural-network-architectures/
│
├── README.md
│
├── requirements.txt
│
├── datasets/
│   └── README.md
│
├── lenet/
│   ├── lenet5_mnist.ipynb
│   └── README.md
│
├── alexnet/
│   ├── alexnet_cifar10.ipynb
│   └── README.md
│
├── vgg/
│   ├── vgg16_cifar10.ipynb
│   └── README.md
│
├── resnet/
│   ├── resnet18_cifar10.ipynb
│   └── README.md
│
└── utils/
    ├── data_utils.ipynb
    └── visualization_utils.ipynb
```