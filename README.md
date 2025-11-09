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


# Week 13: Recurrent Neural Networks (RNNs) and LSTMs

## 📘 Summary
This project explores **Recurrent Neural Networks (RNNs)** and **Long Short-Term Memory (LSTM)** models for sequence and time-series prediction tasks.  
It includes theoretical understanding, hands-on implementation using synthetic data, and a client project predicting real stock prices (**Netflix - NFLX.csv**) using LSTM.

---

## 🧠 Theory Overview

### Recurrent Neural Networks (RNNs)
- Designed to handle **sequential or time-dependent data**.
- Uses **loops** to retain information from previous steps.
- Suitable for text, speech, and stock price prediction.

### Long Short-Term Memory (LSTM)
- A type of RNN that solves the **vanishing gradient problem**.
- Uses gates (Forget, Input, Output) to control memory flow.
- Effective for long-term dependencies in sequences.

---

## 🧩 Model Overview
- **Model Used:** LSTM Neural Network  
- **Dataset:** Netflix stock price data (`Close` column)  
- **Training Ratio:** 80% training, 20% testing  
- **Input Window:** Previous 60 days → predict next day price  

---

## 🏗 Model Architecture

| Layer | Details |
|-------|----------|
| LSTM | 50 units, return_sequences=True |
| LSTM | 50 units |
| Dense | 25 neurons |
| Dense | 1 neuron (output) |
| Optimizer | Adam |
| Loss | Mean Squared Error |

---

## 📊 Results
- **Root Mean Squared Error (RMSE):** ~2–3 depending on run.  
- **Visualization:** Displays training, validation, and predicted stock prices.  
- The model captures stock price trends effectively using temporal dependencies.

---

## ⚙️ How to Run

1. Place your dataset file (e.g., `NFLX.csv`) in the same directory.
2. Run the Python script:
   ```bash
   python week_13_recurrent_neural_networks_(rnns)_and_lstms.py

