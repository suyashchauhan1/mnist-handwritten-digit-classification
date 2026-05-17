# MNIST Handwritten Digit Classification

A Deep Learning project for handwritten digit recognition using the MNIST dataset and TensorFlow/Keras.

This model classifies grayscale handwritten digits from **0–9** with high accuracy using an Artificial Neural Network (ANN).

---

# Overview

The MNIST dataset is one of the most popular beginner datasets in Machine Learning and Deep Learning.

This project demonstrates:

- image preprocessing
- neural network creation
- model training
- prediction
- evaluation
- visualization of learning performance

The model is trained on handwritten digit images and predicts the correct digit class.

---

# Dataset

Dataset Used:

- MNIST Handwritten Digits Dataset

Dataset Details:

| Split | Number of Images |
|---|---|
| Training | 60,000 |
| Testing | 10,000 |

Image Specifications:

- 28 × 28 grayscale images
- Pixel range: 0–255
- Classes: Digits 0–9

---

# Model Architecture

The project uses a Sequential Neural Network built using TensorFlow/Keras.

Architecture:

```text
Input Layer (28x28)
↓
Flatten Layer
↓
Dense Layer (128 neurons, ReLU)
↓
Dropout Layer (0.2)
↓
Dense Layer (32 neurons, ReLU)
↓
Dropout Layer (0.2)
↓
Output Layer (10 neurons, Softmax)
```

---

# Workflow

## 1. Import Libraries

Libraries used:

- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

---

## 2. Load Dataset

The MNIST dataset is loaded directly from TensorFlow/Keras datasets.

```python
from tensorflow.keras.datasets import mnist
```

---

## 3. Data Preprocessing

The images are normalized to improve training performance.

```python
x_train = x_train / 255
x_test = x_test / 255
```

---

## 4. Model Building

The ANN model is created using:

- Flatten layer
- Dense layers
- Dropout layers
- Softmax output layer

---

## 5. Model Compilation

Loss Function:

```python
sparse_categorical_crossentropy
```

Optimizer:

```python
Adam
```

Metric:

```python
accuracy
```

---

## 6. Training

The model is trained for:

```text
10 Epochs
```

with validation data.

---

## 7. Prediction

The model predicts handwritten digits using:

```python
model.predict()
```

---

## 8. Evaluation

Accuracy is calculated using:

```python
accuracy_score(y_test, y_pred)
```

---

# 📊 Results

## Final Test Accuracy

```text
97.58%
```

The model successfully classifies handwritten digits with high accuracy.

---

# 📈 Training Performance

The project also visualizes:

- Training Loss
- Validation Loss
- Training Accuracy
- Validation Accuracy

using Matplotlib graphs.

---

# Sample Prediction

Example:

```text
Input Image → Predicted Digit
```

```text
Handwritten Digit Image → Prediction: 6
```

---

# Tech Stack

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

---

# Model Saving

The trained model is saved using:

```python
model.save('mnist_model.keras')
```

This stores:

- model architecture
- weights
- optimizer state

---

# Run the Project

Clone the repository:

```bash
git clone <your-repository-link>
```

Move into project folder:

```bash
cd <project-folder>
```

Install dependencies:

```bash
pip install tensorflow matplotlib scikit-learn
```

Run Jupyter Notebook:

```bash
jupyter notebook
```

---

# Future Improvements

- CNN-based architecture
- Real-time digit drawing canvas
- Better hyperparameter tuning
- Data augmentation
- Model deployment using Flask/Streamlit
- Mobile compatibility

---

# License

MIT License

---

