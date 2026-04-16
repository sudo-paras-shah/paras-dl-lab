# 📘 Experiment 10: Image Classification using Vision Transformers (ViT)

## 📌 Overview

This experiment focuses on implementing an image classification model using the **Vision Transformer (ViT)** architecture and comparing its performance with a **ResNet-18 CNN model**.

The study explores how transformer-based models differ from traditional convolutional networks and evaluates the impact of **data augmentation, loss functions, and optimizers** on model performance.

---

## 🎯 Objective

* Implement a Vision Transformer (ViT) for image classification
* Compare ViT with a ResNet-18 model
* Analyze the effect of:

  * Data augmentation
  * Different loss functions
  * Various optimizers
* Track and evaluate model performance

---

## 📂 Dataset

* **Dataset Used:** CIFAR-10
* **Split:**

  * 80% Training
  * 10% Validation
  * 10% Testing

---

## ⚙️ Preprocessing & Augmentation

### Preprocessing

* Normalization
* Resizing (if required)

### Data Augmentation

* Horizontal Flip
* Vertical Flip

Models are trained on:

* Original dataset
* Augmented dataset

---

## 🧠 Models Implemented

### 1. Vision Transformer (ViT)

* Patch Embedding (4×4 / 8×8 patches)
* Positional Encoding
* Transformer Encoder:

  * Multi-head Self-Attention
  * Feed-forward Network
  * Layer Normalization & Residual Connections
* CLS Token for classification
* Fully connected classification head

### 2. ResNet-18 (CNN Baseline)

* Standard convolutional neural network
* Same preprocessing and augmentation as ViT

---

## 🔬 Experiments Conducted

### Loss Functions

* Cross-Entropy Loss
* Label Smoothing Loss
* Focal Loss

### Optimizers

* SGD
* RMSprop
* Adam

### Comparisons

* ViT vs ResNet-18
* With vs Without Augmentation
* Different Loss Functions
* Different Optimizers

---

## 📊 Training & Tracking

* Metrics tracked:

  * Training Loss
  * Validation Loss
  * Accuracy
* Experiment tracking using **Weights & Biases (W&B)**

---

## 📈 Evaluation Metrics

* Test Accuracy
* Training Time
* Model Complexity

---

## 📌 Results & Analysis

### Data Augmentation

* Improves generalization
* Reduces overfitting
* Helps models learn invariant features

### ViT vs ResNet-18

* CNNs perform better on smaller datasets due to inductive bias
* ViTs capture global relationships using attention
* ViTs perform better with more data and training

### Loss Functions

* Cross-Entropy: Stable and widely used
* Label Smoothing: Improves generalization
* Focal Loss: Focuses on hard examples

### Optimizers

* SGD: Better generalization, slower convergence
* RMSprop: Faster convergence
* Adam: Adaptive learning, widely effective

---

## 🚀 Expected Outcomes

* Improved performance with augmentation
* Better understanding of transformer vs CNN architectures
* Insight into optimization and loss strategies
* Hands-on experience with experiment tracking tools

---

## 🛠️ Tech Stack

* Python
* PyTorch
* NumPy
* Matplotlib
* Weights & Biases

---

## 📚 References

* Vision Transformer (ViT) Paper
* PyTorch Documentation
* CIFAR-10 Dataset
