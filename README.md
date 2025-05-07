# 🧠 PixelCNN on MNIST
A PyTorch implementation of the **PixelCNN** model for generative image modeling on the **MNIST** dataset. This project demonstrates how PixelCNN learns pixel-wise dependencies to generate realistic handwritten digits.

![PixelCNN Output](./assets/output.png)

---

## 📌 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Details](#training-details)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgements](#acknowledgements)

---

## 🧾 Overview

PixelCNN is an autoregressive deep learning model that generates images **pixel-by-pixel**, predicting the value of each pixel conditioned on previously generated pixels. In this project:

- PixelCNN is implemented **from scratch** using **PyTorch**.
- The model is trained on **binarized MNIST** digits.
- We visualize generated images at various epochs to assess generative quality.

---

## 📚 Dataset

We use the classic **MNIST** dataset consisting of handwritten digits:

- 60,000 training images
- 10,000 testing images
- Each image is 28x28 grayscale

Images are binarized using a threshold of `0.5`.

---

## 🧱 Model Architecture

- Custom **masked convolutions** (`Mask-A` and `Mask-B`)
- **Residual blocks** to stabilize and enhance learning
- Autoregressive prediction using **pixel-by-pixel generation**

Total trainable parameters: **~492,673**

---

## ⚙️ Training Details

- Optimizer: `Adam`
- Loss: `Binary Cross-Entropy (BCE)`
- Batch size: `64`
- Device: GPU/CPU supported
- Epochs: `30`

### 📉 Loss Curves

![Loss Curve](./assets/asd.png)

---

## 🎨 Results

### Generated Samples After 10 Epochs
![Generated at 10 Epochs](./assets/asddas.png)

### Generated Samples After 20 Epochs
![Generated at 20 Epochs](./assets/asddas.png)

### Generated Samples After 30 Epochs
![Generated at 30 Epochs](./assets/output.png)

> With more epochs, the digits become sharper and more recognizable.

---

## 🙏 Acknowledgements
Inspired by the original PixelCNN paper by van den Oord et al.

MNIST dataset from Yann LeCun's website