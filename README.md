# Neural Networks

This repository contains implementations of fundamental neural network concepts built from scratch using Python and NumPy.

The notebook demonstrates two approaches:

1. **Simple Perceptron** using the Iris dataset
2. **Multi-Layer Perceptron (MLP)** using the XOR problem

The implementations focus on understanding how weights, biases, activation functions, forward propagation, and backpropagation work internally.

## 📌 Contents

### 1. Simple Perceptron

The first part implements a basic perceptron for binary classification.

**Details:**

* Dataset: Iris Dataset
* Input features: First two Iris features
* Classes used: Iris classes 0 and 1
* Activation function: Step function
* Train/Test Split: 70/30
* Weight initialization: `[1, 1]`
* Learning rate: `0.2`
* Manual weight update
* Accuracy calculation

The perceptron predicts the output using a weighted sum of the input features followed by a step activation function.

The weights are updated when the prediction differs from the target.

## 🧠 Perceptron Learning Rule

The weight update is implemented as:

```text
new_weight = weight + (error × learning_rate × input)
```

where:

```text
error = target - prediction
```

The implementation and evaluation are performed manually using NumPy.

---

### 2. Multi-Layer Perceptron

The second part implements a small neural network from scratch to solve the **XOR problem**.

**Architecture:**

```text
Input Layer       Hidden Layer       Output Layer

   x1 ──────────►   H1 ──────────┐
                    │             │
   x2 ──────────►   H2 ──────────┼──► Output
                                  │
```

**Network configuration:**

* Input neurons: 2
* Hidden layers: 1
* Hidden neurons: 2
* Output neurons: 1
* Activation function: Sigmoid
* Dataset: XOR
* Learning rate: `1`
* Training epochs: `1,000,000`

The network uses randomly initialized weights and zero-initialized biases.

## 🔄 Forward Propagation

The notebook manually calculates:

1. Weighted sums for the hidden neurons
2. Sigmoid activation for the hidden layer
3. Weighted sum for the output neuron
4. Sigmoid activation for the final output
5. Mean squared error-style loss

The loss is calculated as:

```text
Loss = 1/2 × (output - target)²
```

## 🔙 Backpropagation

The MLP also implements backpropagation manually.

The notebook calculates gradients for:

* Output-layer weights
* Hidden-layer weights
* Hidden-layer biases
* Output bias

The calculated gradients are then used to update the weights and biases using gradient descent.

## 📊 XOR Results

After training, the network produces the following predictions:

| Input    | Target |  Output | Prediction |
| -------- | -----: | ------: | ---------: |
| `[0, 0]` |      0 | ~0.0011 |          0 |
| `[0, 1]` |      1 | ~0.9990 |          1 |
| `[1, 0]` |      1 | ~0.9988 |          1 |
| `[1, 1]` |      0 | ~0.0010 |          0 |

The trained network correctly classifies all four XOR inputs in the recorded notebook output.

## 🛠️ Technologies Used

* Python
* NumPy
* Scikit-learn
* Google Colab

## 📂 Repository Structure

```text
Neural-Networks/
│
├── Perceptron_and_MLP.ipynb
└── README.md
```

## 🎯 Objective

The objective of this notebook is to understand the fundamental working of neural networks by implementing the learning process manually instead of relying on a high-level neural network library.

The implementations demonstrate how a perceptron performs binary classification and how a multi-layer neural network can learn a non-linear problem such as XOR.

## 📚 Concepts Demonstrated

* Perceptron
* Weights and biases
* Step activation function
* Sigmoid activation function
* Forward propagation
* Loss calculation
* Backpropagation
* Gradient calculation
* Gradient descent
* Weight updates
* Binary classification
* Neural network learning

## 👨‍💻 Author

**Bhanu Kishore**
B.Tech – Artificial Intelligence & Data Science

