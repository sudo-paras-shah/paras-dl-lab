---

# Experiment 9: Generative Adversarial Networks (GANs)

## 📌 Overview

This project implements **Generative Adversarial Networks (GANs)** for image generation using the Fashion-MNIST dataset. The experiment explores different GAN variants, including **Vanilla GAN** and **Deep Convolutional GAN (DCGAN)**, and analyzes their performance under various configurations.

---

## 🎯 Objective

* Implement GAN and DCGAN architectures using PyTorch
* Compare model performance based on architecture, loss functions, and optimizers
* Analyze training stability, convergence, and generated outputs

---

## 📂 Dataset

* **Fashion-MNIST**
* Grayscale images of size **28×28** representing clothing items
* Data is normalized to the range **[-1, 1]**

---

## ⚙️ Model Architectures

### 1. Generator

* Input: Random noise (latent vector)
* Output: Generated image

**Vanilla GAN:**

* Fully connected layers

**DCGAN:**

* Transposed convolution layers
* Batch normalization
* ReLU activation

---

### 2. Discriminator

* Input: Image (real or fake)
* Output: Probability of being real

**Vanilla GAN:**

* Fully connected layers

**DCGAN:**

* Convolutional layers
* LeakyReLU activation

---

## 🔁 Training Process

* Alternating training of generator and discriminator
* Discriminator learns to distinguish real vs fake images
* Generator learns to fool the discriminator
* Metrics tracked:

  * Generator loss
  * Discriminator loss

---

## 🧪 Experiments

### Loss Functions

* Binary Cross-Entropy (BCE)
* Least Squares GAN (LSGAN)
* Wasserstein Loss (WGAN)

### Optimizers

* SGD
* RMSprop
* Adam

---

## 📊 Evaluation Metrics

* Visual quality of generated images
* Diversity of outputs
* Training stability and convergence

---

## 🔍 Observations

* DCGAN produces higher-quality and more stable outputs than Vanilla GAN
* Adam optimizer provides better convergence
* Loss functions significantly impact stability
* Common challenges observed:

  * Mode collapse
  * Vanishing gradients
  * Oscillations during training

---

## 📈 Tools Used

* PyTorch
* Weights & Biases (for experiment tracking)
* Hugging Face (for model hosting)

---

## ✅ Conclusion

This experiment demonstrates how GANs learn to generate realistic images through adversarial training. It highlights the importance of architecture design, loss functions, and optimizers in achieving stable and high-quality results.

---

