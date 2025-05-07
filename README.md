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
![output](https://github.com/user-attachments/assets/0423cef2-7abe-4a4e-8d74-96b5af2211f4)

---

## 🎨 Results

### Generated Samples After 20 Epochs
![asddas](https://github.com/user-attachments/assets/67c084c1-eea9-4d7d-9ef4-bac99a0103ae)


### Generated Samples After 30 Epochs
![asd](https://github.com/user-attachments/assets/ed31dd3b-fd23-46ae-909d-be147c07dff7)


> With more epochs, the digits become sharper and more recognizable.

---

## 🙏 Acknowledgements
Inspired by the original PixelCNN paper by van den Oord et al.

MNIST dataset from Yann LeCun's website
