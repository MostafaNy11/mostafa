#  MNIST Handwritten Digit Classification

This project implements a neural network for handwritten digit classification using the MNIST dataset. Two different activation functions (**ReLU** and **Tanh**) are tested and compared to evaluate their impact on model performance.

---

##  Project Overview

The goal of this project is to classify handwritten digits (0–9) from the MNIST dataset using Artificial Neural Networks (ANN).

The project includes:

- Data preprocessing
- Model training
- Performance evaluation
- Confusion Matrix visualization
- Accuracy/Loss curves
- Comparison between activation functions

---

##  Dataset

MNIST dataset:

- 60,000 training images
- 10,000 testing images
- Image size: **28×28**
- Grayscale handwritten digits
- Classes: **0–9**

Dataset loaded using:

```python
from tensorflow.keras.datasets import mnist
```

---

## 🛠 Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Matplotlib
- Seaborn
- TensorFlow / Keras
- Scikit-learn

---

## ⚙️ Data Preprocessing

Steps applied:

- Normalize pixel values from:

```text
0–255 → 0–1
```

- Convert labels using One-Hot Encoding:

```python
to_categorical()
```

---

##  Model Architecture

### Model 1 — ReLU Activation

Architecture:

```text
Flatten Layer
↓
Dense(128, activation='relu')
↓
Dropout(0.2)
↓
Dense(10, activation='softmax')
```

---

### Model 2 — Tanh Activation

Architecture:

```text
Flatten Layer
↓
Dense(128, activation='tanh')
↓
Dropout(0.2)
↓
Dense(10, activation='softmax')
```

---

##  Training Configuration

```python
Optimizer: Adam
Loss Function: Categorical Crossentropy
Epochs: 10
Validation Split: 20%
```

---

##  Evaluation

The project evaluates:

- Test accuracy
- Test loss
- Predictions on unseen images
- Confusion Matrix
- Accuracy curves
- Loss curves

---

##  Visualization

Implemented visualizations:

- Sample digit display
- Predictions vs actual labels
- Confusion Matrix heatmap
- Training & validation accuracy curves
- Training & validation loss curves

---

##  Project Structure

```text
MNIST_Project/
│
├── MNIST_Project.ipynb
├── README.md
└── requirements.txt
```

---

##  Run Project

Clone repository:

```bash
git clone https://github.com/your-username/MNIST_Project.git
```

Move to project:

```bash
cd MNIST_Project
```

Install packages:

```bash
pip install -r requirements.txt
```

Run notebook:

```bash
jupyter notebook
```

Open:

```text
MNIST_Project.ipynb
```

---

##  Experiment Goal

The main purpose of this project is to compare the effect of different activation functions (**ReLU vs Tanh**) on handwritten digit classification performance.

---

##  License

Educational project for learning Deep Learning concepts.
