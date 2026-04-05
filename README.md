# AI-Powered Steganalysis: Detecting PVD-Based Hidden Data 🚀
# Dataset Link: https://www.kaggle.com/datasets/petrdufek/stego-pvd-dataset

## 📌 Project Overview

This project focuses on **digital forensics and cybersecurity**, aiming to detect hidden information embedded within digital images. Specifically, it targets **PVD (Pixel Value Differencing) steganography**, a technique used to conceal data by modifying pixel intensity differences.

The goal of this system is to build an intelligent **steganalysis model** capable of distinguishing between:

* **Clean Images** (no hidden data)
* **Stego Images** (containing hidden data)

---

## 🧠 Technical Challenge

Steganalysis is inherently challenging due to the following reasons:

* **Subtle Patterns**
  PVD introduces extremely small pixel variations that are difficult to detect, even for standard CNN models.

* **Noise vs. Hidden Data**
  Natural image textures and embedded data noise overlap, making it hard for models to differentiate between them.

---

## 🔬 Proposed Methodology & Architecture

To overcome these challenges, the following advanced techniques are implemented:

### 🔹 SRM (Spatial Rich Model) Filters

* A custom preprocessing layer applies **SRM filters** at the input stage
* These filters extract **noise residuals** from images
* Helps highlight hidden data patterns that are otherwise invisible

---

### 🔹 Residual CNN Design

* Incorporates **skip connections (residual connections)**
* Prevents information loss in deep networks
* Improves gradient flow and training stability

---

### 🔹 Regularization Techniques

To avoid overfitting:

* **Dropout (0.5)** is applied to reduce dependency on specific neurons
* **Batch Normalization** stabilizes and accelerates training

---

### 🔹 Dynamic Learning Strategy

* Uses **ReduceLROnPlateau** callback
* Automatically reduces learning rate when validation loss stops improving
* Ensures better convergence and performance

---

## 📊 Dataset Details

* **Total Images:** ~16,000
* **Training Set:** 8,000 images
* **Validation Set:** 4,000 images
* **Test Set:** 4,000 images

### 🔹 Classes:

* **Clean:** Images without hidden data
* **Stego:** Images containing hidden data using PVD

### 🔹 Image Size:

* 256 × 256 pixels

---

## 🛠️ Tech Stack

* **Programming Language:** Python
* **Deep Learning Framework:** TensorFlow / Keras
* **Data Processing:** NumPy, ImageDataGenerator
* **Visualization:** Matplotlib

---

## 🚀 Key Features

* Detects hidden data in images using advanced deep learning techniques
* Utilizes SRM filters for enhanced noise pattern extraction
* Employs residual connections for improved deep network performance
* Includes regularization methods to prevent overfitting
* Implements adaptive learning rate for efficient training

---

## 🎯 Conclusion

This project demonstrates how **AI-driven steganalysis** can effectively detect hidden data in images, even when advanced techniques like PVD are used. By combining SRM filters, residual CNN architecture, and adaptive learning strategies, the model achieves strong performance in identifying subtle hidden patterns.

---
