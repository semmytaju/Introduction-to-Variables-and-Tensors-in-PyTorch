# Introduction to Variables and Tensors in PyTorch

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)
![License](https://img.shields.io/badge/License-MIT-green)
![Google Colab](https://img.shields.io/badge/Google-Colab-orange)

A beginner-friendly yet comprehensive introduction to **PyTorch Tensors**, **Automatic Differentiation (Autograd)**, and **GPU Acceleration**. This repository is designed for students, researchers, and machine learning practitioners who want to learn the fundamentals of PyTorch before moving on to neural networks and deep learning.

---

## 📚 Overview

PyTorch is one of the most popular deep learning frameworks used in both academia and industry. It provides:

- Tensor computation with GPU acceleration
- Automatic differentiation (Autograd)
- Dynamic computational graphs
- Flexible deep learning model development

This tutorial introduces the building blocks of PyTorch:

- Tensors
- Tensor operations
- Shapes and dimensions
- Data types
- Automatic differentiation
- Gradient computation
- GPU acceleration

---

## 🎯 Learning Objectives

After completing this tutorial, you will be able to:

✅ Understand what a Tensor is in PyTorch

✅ Create and manipulate tensors

✅ Understand tensor shapes and dimensions

✅ Work with different tensor data types

✅ Perform tensor operations

✅ Understand Automatic Differentiation (Autograd)

✅ Compute gradients using backpropagation

✅ Utilize GPU acceleration

---

## 📂 Repository Structure

```text
Introduction-to-Variables-in-PyTorch/

│
├── notebooks/
│   └── Introduction_to_Variables_in_PyTorch.ipynb
│
├── images/
│
├── README.md
│
├── requirements.txt
│
└── LICENSE
```

---

## 🛠️ Prerequisites

Basic knowledge of:

- Python Programming
- Variables and Functions
- Linear Algebra (Vectors and Matrices)

Recommended:

- NumPy

---

## 🚀 Installation

### Option 1: Google Colab

Open the notebook directly in Google Colab.

PyTorch is already installed in most Colab environments.

Verify installation:

```python
import torch

print(torch.__version__)
```

---

### Option 2: Local Installation

Install PyTorch:

```bash
pip install torch torchvision torchaudio
```

Verify installation:

```python
import torch

print(torch.__version__)
```

---

## 📖 Topics Covered

### 1. Introduction to Tensors

- Scalar
- Vector
- Matrix
- Higher-dimensional Tensors

---

### 2. Tensor Creation

Examples:

```python
torch.tensor()
torch.zeros()
torch.ones()
torch.rand()
torch.randn()
```

---

### 3. Tensor Shape and Dimensions

Understanding:

```python
tensor.shape
tensor.ndim
```

---

### 4. Tensor Data Types

Common dtypes:

| Type | Description |
|--------|--------|
| torch.int32 | Integer |
| torch.int64 | Long Integer |
| torch.float32 | Float |
| torch.float64 | Double Precision Float |
| torch.bool | Boolean |

---

### 5. Tensor Operations

Operations covered:

- Addition
- Subtraction
- Multiplication
- Division
- Matrix Multiplication

Example:

```python
torch.matmul(A, B)
```

---

### 6. Tensor Reshaping

Examples:

```python
reshape()
view()
flatten()
```

---

### 7. NumPy Interoperability

Converting:

- NumPy → Tensor
- Tensor → NumPy

---

### 8. Automatic Differentiation (Autograd)

PyTorch's automatic gradient computation engine.

Example:

```python
x = torch.tensor(
    2.0,
    requires_grad=True
)

y = x**2

y.backward()

print(x.grad)
```

Expected Output:

```text
tensor(4.)
```

---

### 9. Gradient Computation

Computing derivatives automatically:

```python
dy/dx
```

using:

```python
.backward()
```

---

### 10. GPU Acceleration

Check GPU availability:

```python
torch.cuda.is_available()
```

Move tensors to GPU:

```python
x = x.to("cuda")
```

---

## ▶️ Running the Notebook

Launch Jupyter:

```bash
jupyter notebook
```

Open:

```text
Introduction_to_Variables_in_PyTorch.ipynb
```

Run all cells sequentially.

---

## 💡 Example: Creating Your First Tensor

```python
import torch

x = torch.tensor([
    [1, 2, 3],
    [4, 5, 6]
])

print(x)
print(x.shape)
print(x.ndim)
```

Output:

```text
tensor([[1, 2, 3],
        [4, 5, 6]])

torch.Size([2, 3])

2
```

---

## 🔥 Example: Automatic Differentiation

```python
import torch

x = torch.tensor(
    5.0,
    requires_grad=True
)

y = 3*x**2 + 2*x + 1

y.backward()

print(x.grad)
```

Output:

```text
tensor(32.)
```

---

## ⚡ Example: GPU Acceleration

```python
import torch

device = torch.device(
    "cuda" if torch.cuda.is_available()
    else "cpu"
)

x = torch.rand((3,3)).to(device)

print(x.device)
```

Output:

```text
cuda:0
```


## 📚 References

### Official PyTorch Documentation

- https://pytorch.org/docs/stable/
- https://pytorch.org/tutorials/
- https://pytorch.org/docs/stable/tensors.html
- https://pytorch.org/docs/stable/autograd.html

---

## 📖 Recommended Books

### Deep Learning

Goodfellow, Bengio, Courville

**Deep Learning**

https://www.deeplearningbook.org/

---

### Deep Learning with PyTorch

Eli Stevens, Luca Antiga, Thomas Viehmann

Manning Publications

---

### Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow

Aurélien Géron

O'Reilly Media

---

## 📄 Research Papers

### PyTorch

Adam Paszke et al. (2019)

**PyTorch: An Imperative Style, High-Performance Deep Learning Library**

NeurIPS 2019

https://papers.neurips.cc/paper_files/paper/2019/hash/bdbca288fee7f92f2bfa9f7012727740-Abstract.html

---
