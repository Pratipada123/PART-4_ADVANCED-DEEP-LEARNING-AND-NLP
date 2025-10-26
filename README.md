# 🧠 Convolutional Neural Network (CNN) for Image Classification

## 📘 Project Overview
This project demonstrates how to build, train, and evaluate a **Convolutional Neural Network (CNN)** for **image classification** using the **CIFAR-10 dataset**.

The model automatically learns to extract visual features such as edges, textures, and shapes, and classifies images into **10 categories**:
> airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck.

---

## 🎯 Objective
The goal is to:
- Build a CNN model from scratch using **TensorFlow/Keras**
- Train it on the **CIFAR-10 dataset**
- Evaluate its performance (accuracy and loss)
- Visualize training progress and make predictions

---

## 🧩 Dataset: CIFAR-10
- **Total Images:** 60,000 color images (32×32 pixels)
- **Training:** 50,000 images  
- **Testing:** 10,000 images  
- **Classes (10):**
  - airplane  
  - automobile  
  - bird  
  - cat  
  - deer  
  - dog  
  - frog  
  - horse  
  - ship  
  - truck  

---

## ⚙️ Technologies Used
| Tool | Purpose |
|------|----------|
| **Python 3.x** | Programming language |
| **TensorFlow / Keras** | Deep learning framework |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |

---

## 🚀 Model Architecture
The CNN is built using **Sequential API** in Keras.

### **Model Layers**
| Layer | Type | Purpose | Example |
|-------|------|----------|----------|
| 1 | **Conv2D** | Extracts features from the image | `Conv2D(32, (3,3), activation='relu')` |
| 2 | **MaxPooling2D** | Reduces spatial dimensions | `MaxPooling2D((2,2))` |
| 3 | **Conv2D** | Deeper feature extraction | `Conv2D(64, (3,3), activation='relu')` |
| 4 | **MaxPooling2D** | More downsampling | `MaxPooling2D((2,2))` |
| 5 | **Conv2D** | Detects high-level features | `Conv2D(64, (3,3), activation='relu')` |
| 6 | **Flatten** | Converts 2D data → 1D vector | `Flatten()` |
| 7 | **Dense** | Fully connected layer | `Dense(64, activation='relu')` |
| 8 | **Dense (Output)** | Predicts class probabilities | `Dense(10, activation='softmax')` |

---

## 🧮 Model Summary
```text
Layer (type)                 Output Shape              Param #
=================================================================
conv2d (Conv2D)              (32, 32, 3) → (30, 30, 32)   896
max_pooling2d (MaxPooling2D) (30, 30, 32) → (15, 15, 32)  0
conv2d_1 (Conv2D)            (15, 15, 32) → (13, 13, 64)  18496
max_pooling2d_1 (MaxPooling) (13, 13, 64) → (6, 6, 64)    0
conv2d_2 (Conv2D)            (6, 6, 64) → (4, 4, 64)      36928
flatten (Flatten)            (4, 4, 64) → (1024)          0
dense (Dense)                (1024 → 64)                  65600
dense_1 (Dense)              (64 → 10)                    650
=================================================================
Total params: 122,570
Trainable params: 122,570
Non-trainable params: 0
