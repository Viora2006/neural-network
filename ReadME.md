# Neural Network From Scratch (NumPy)

## Overview

This project is a simple feedforward neural network built entirely from scratch using Python and NumPy. The network is trained using backpropagation and gradient descent to learn the XOR logical operation.

The purpose of this project is educational: to understand how neural networks work internally without relying on machine learning frameworks such as TensorFlow or PyTorch.

---

## Features

- Custom neural network implementation
- Fully connected (dense) layers
- ReLU activation function
- Sigmoid activation function
- Forward propagation
- Backpropagation
- Gradient descent optimization
- Mean Squared Error (MSE) loss
- XOR dataset training example

---

## Project Structure

```text
.
├── main.py
├── network.py
├── network_layer.py
└── activation_function.py
```

### main.py

Creates the XOR dataset, builds the network architecture, trains the model, and displays predictions.

### network.py

Contains the `Network` class responsible for:

- Managing layers
- Running forward propagation
- Running backpropagation
- Training the model

### network_layer.py

Contains the `Layer` class responsible for:

- Weight initialization
- Bias initialization
- Forward propagation
- Gradient calculations
- Parameter updates

### activation_function.py

Contains activation functions:

- `ReLU`
- `Sigmoid`

Each activation includes both forward and backward methods.

---

## Network Architecture

```text
Input Layer (2 neurons)
        ↓
Hidden Layer (8 neurons)
        ↓
ReLU Activation
        ↓
Output Layer (1 neuron)
        ↓
Sigmoid Activation
```

---

## XOR Dataset

Training inputs:

```python
X = np.array([
    [0, 0],
    [0, 1],
    [1, 0],
    [1, 1]
])
```

Expected outputs:

```python
y = np.array([
    [0],
    [1],
    [1],
    [0]
])
```

The network learns to output `1` when the inputs are different and `0` when they are the same.

---

## Training

The network is trained using:

- Mean Squared Error (MSE)
- Backpropagation
- Gradient Descent

Example configuration:

```python
network.train(X, y, epochs=10000, learning_rate=0.1)
```

---

## Example Output

```text
Epoch 0 | Loss: 0.2512
Epoch 1000 | Loss: 0.0313
Epoch 2000 | Loss: 0.0064
Epoch 3000 | Loss: 0.0031
Epoch 4000 | Loss: 0.0020
Epoch 5000 | Loss: 0.0015
Epoch 6000 | Loss: 0.0011
Epoch 7000 | Loss: 0.0009
Epoch 8000 | Loss: 0.0008
Epoch 9000 | Loss: 0.0007

Predictions:
[[0.04147633]
 [0.98396849]
 [0.98396733]
 [0.01117949]]
```

The predictions closely match the expected XOR outputs:

```text
[0]
[1]
[1]
[0]
```

---

## Technologies Used

- Python
- NumPy

---

## Learning Goals

This project demonstrates:

- Matrix multiplication in neural networks
- Weight and bias initialization
- Activation functions
- Forward propagation
- Backpropagation
- Gradient descent optimization
- Loss calculation
- Basic machine learning concepts

---

## Future Improvements

Potential enhancements include:

- Multiple hidden layers
- Additional activation functions
- Cross-entropy loss
- Mini-batch gradient descent
- Saving and loading trained models
- Visualization of training progress
- Support for larger datasets

---

## Author

**Tyler Carrasco**

Built as a learning project to understand the mathematics and implementation details behind neural networks.