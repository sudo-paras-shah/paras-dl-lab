# Experiment 8: Autoencoders and Variational Autoencoders (VAE)

## 📌 Overview

This experiment focuses on implementing and comparing **Autoencoders (AE)** and **Variational Autoencoders (VAE)** to learn latent representations and generate data. The study highlights differences between deterministic and probabilistic models, and evaluates how architectural and training choices impact performance.

---

## 🎯 Objectives

* Implement Autoencoder and Variational Autoencoder using PyTorch
* Learn latent representations of image data
* Compare reconstruction and generation capabilities
* Analyze:

  * Latent space dimensionality
  * Loss functions (MSE vs BCE)
  * Optimizers (SGD, RMSprop, Adam)
  * Deterministic vs probabilistic modeling

---

## 📂 Dataset

* **Fashion-MNIST**

  * Grayscale images of clothing items (e.g., shirts, shoes, bags)
* Data Split:

  * 80% Training
  * 10% Validation
  * 10% Testing

---

## ⚙️ Preprocessing

* Normalize pixel values to `[0, 1]`
* Flatten images (for fully connected networks) or retain shape (for CNNs)

---

## 🧠 Model Architectures

### 🔹 Autoencoder (AE)

* **Encoder**: Maps input image → latent vector
* **Decoder**: Reconstructs image from latent vector
* **Loss Functions**:

  * Mean Squared Error (MSE)
  * Binary Cross Entropy (BCE)

---

### 🔹 Variational Autoencoder (VAE)

* Learns **probabilistic latent distribution**
* Outputs:

  * Mean (μ)
  * Variance (σ)

#### Reparameterization Trick:

```
z = μ + σ · ε,   ε ~ N(0,1)
```

#### Loss Function:

* Reconstruction Loss (MSE/BCE)
* KL Divergence:

```
D_KL(q(z|x) || p(z))
```

---

## 🔬 Experiments

### 1. Latent Space Dimension

Test multiple sizes:

* 2, 8, 16, 32

Evaluate:

* Reconstruction quality
* Latent space structure

---

### 2. Latent Space Interpolation

Interpolate between two latent vectors:

```
z_interp = (1 - α)z₁ + αz₂,   α ∈ [0,1]
```

* Generate intermediate images
* Analyze smooth transitions between classes

---

### 3. Optimizers

Train models using:

* SGD
* RMSprop
* Adam

Compare:

* Convergence speed
* Stability

---

## 📊 Experiment Tracking

* Track:

  * Training loss
  * Validation loss
  * Reconstruction error
* Use **Weights & Biases (W&B)** for logging

---

## 📦 Deliverables

* GitHub repository (code + README)
* Weights & Biases project link
* Hugging Face model link (trained models + outputs)

---

## 📈 Evaluation Criteria

* Reconstruction quality
* Latent space smoothness
* Data generation capability
* Interpolation quality

Comparisons:

* Autoencoder vs VAE
* Latent dimensions
* Loss functions
* Optimizers

---

## 🧩 Analysis & Discussion

### Autoencoder vs VAE

* AE: Deterministic representation
* VAE: Probabilistic latent space → smoother generation

### Latent Space

* Effect of dimension size
* Visualization (especially 2D case)
* Continuity across categories

### Loss Functions

* BCE → sharper reconstructions
* MSE → smoother outputs

### Optimizers

* Adam → faster convergence
* SGD → slower but stable
* RMSprop → balanced performance

### KL Divergence

* Regularizes latent space
* Trade-off:

  * Better structure vs reconstruction accuracy

---

## 🔍 Observations

* Autoencoders:

  * Better reconstruction sharpness
* VAEs:

  * Better generative capability
  * Smoother latent transitions
* Latent size significantly affects performance

---

## ✅ Expected Outcomes

* Clear understanding of AE vs VAE
* Improved intuition for latent space learning
* Ability to generate new data samples
* Experience with:

  * Experiment tracking
  * Model comparison
  * Generative modeling

---

## 🚀 Tech Stack

* Python
* PyTorch
* Weights & Biases
* Hugging Face

---

## 📎 Notes

* Fashion-MNIST provides a more complex alternative to MNIST
* VAE is preferred for generative tasks due to structured latent space

---

