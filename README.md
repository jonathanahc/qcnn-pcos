# 🧬 Quantum Machine Learning for PCOS Ultrasound Classification using QCNN

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![TensorFlow Quantum](https://img.shields.io/badge/TensorFlow%20Quantum-QML-purple)
![Cirq](https://img.shields.io/badge/Cirq-Quantum-red)
![Research](https://img.shields.io/badge/Research-QCNN-green)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

### Quantum Convolutional Neural Network (QCNN) for the Classification of Polycystic Ovary Syndrome (PCOS) Ultrasound Images

Master's Degree in Artificial Intelligence and Data Analytics  
Universidad Autónoma de Ciudad Juárez (UACJ)

</div>

---

# 📖 Overview

This project investigates the application of Quantum Machine Learning (QML) to the classification of ultrasound images associated with Polycystic Ovary Syndrome (PCOS).

A hybrid quantum-classical architecture based on a Quantum Convolutional Neural Network (QCNN) was developed and evaluated using ultrasound images. The model integrates classical image preprocessing, dimensionality reduction, quantum encoding, quantum convolution and pooling operations, and a final classical classifier.

---

# 🎯 Objectives

- Develop a QCNN model for binary classification of ultrasound images.
- Evaluate the feasibility of Quantum Machine Learning in medical imaging.
- Compare QCNN performance against traditional CNN models.
- Analyze the impact of qubit quantity on classification performance.

---

# 🏗️ Architecture

```mermaid
flowchart LR
A[Ultrasound Images] --> B[Preprocessing]
B --> C[Normalization]
C --> D[PCA Reduction]
D --> E[Quantum Encoding]
E --> F[QCNN Circuit]
F --> G[Pauli-Z Measurement]
G --> H[Dense Layer]
H --> I[Binary Classification]
I --> J[Evaluation Metrics]
```

---

# 📂 Dataset

## Original Dataset

| Class | Images |
|---------|---------:|
| PCOS | 1568 |
| Non-PCOS | 2288 |
| Total | 3856 |

## After Cleaning

- Corrupted images removed: 10
- Duplicate images removed: 1846
- Final dataset: 2000 images

## Balanced Dataset

| Class | Images |
|---------|---------:|
| PCOS | 1000 |
| Non-PCOS | 1000 |

---

# 🔬 Data Preparation

## Image Processing

- Grayscale conversion
- Resize to 128 × 128
- Normalization (0–1)
- Vectorization

## Feature Reduction

Original features:

16,384 pixels per image

Reduced using PCA:

8 principal components

Mapped to:

8 qubits

---

# ⚛️ Quantum Encoding

The reduced feature vector is encoded into a quantum state using:

- Angle Encoding
- RX rotation gates
- 8 Qubits

Each principal component controls a quantum rotation angle.

---

# ⚙️ QCNN Architecture

## Quantum Convolution

- Parametrized RY gates
- Local feature extraction
- Neighbor entanglement

## Entanglement Layer

- CNOT gates
- Information propagation

## Quantum Pooling

- Information compression
- Circuit dimensionality reduction

## Readout

Measured qubits:

- q1
- q3
- q5
- q7

Observable:

- Pauli-Z

---

# 🧠 Hybrid Model

```text
Quantum Circuit
      ↓
Expectation Values
      ↓
Dense Layer (ReLU)
      ↓
Dropout (0.2)
      ↓
Sigmoid Output
```

---

# 🛠️ Technologies

## Quantum Computing

- TensorFlow Quantum
- Cirq
- SymPy

## Machine Learning

- TensorFlow
- Scikit-Learn

## Data Analysis

- NumPy
- Pandas

## Visualization

- Matplotlib
- Seaborn

## Environment

- Google Colab
- Python 3.10

---

# 📊 Experimental Configuration

| Parameter | Value |
|------------|---------|
| Image Size | 128×128 |
| Qubits | 8 |
| Epochs | 50 |
| Batch Size | 16 |
| Learning Rate | 0.01 |
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |

---

# 📈 Results

## QCNN Performance

| Metric | Score |
|----------|---------:|
| Accuracy | 87.00% |
| AUC-ROC | 0.9318 |

## PCOS

| Metric | Value |
|----------|---------:|
| Precision | 89.93% |
| Recall | 83.33% |
| F1-Score | 86.511% |

## Non-PCOS

| Metric | Value |
|----------|---------:|
| Precision | 84.47% |
| Recall | 90.67% |
| F1-Score | 87.46% |

---

# 📉 Limitations

- Simulated quantum environment.
- Limited qubit count.
- PCA dimensionality reduction.
- NISQ hardware constraints.

---

# 🚀 Future Work

- Increase qubit count.
- Evaluate amplitude encoding.
- Test alternative QCNN architectures.
- Execute on real quantum hardware.
- Expand to additional medical imaging tasks.

---

# 📁 Repository Structure

```text
.
├── notebooks/
│   └── QCNN_PCOS.ipynb
├── README.md

```

---

# 👨‍💻 Author

Jonathan Adrian Herrera Castro

M.Sc. Candidate in Artificial Intelligence and Data Analytics

Universidad Autónoma de Ciudad Juárez (UACJ)

Ciudad Juárez, Chihuahua, México

---

# 📚 Citation

```bibtex
@mastersthesis{herrera2026qcnn,
  author = {Jonathan Adrian Herrera Castro},
  title = {Quantum Machine Learning for the Classification of Ultrasound Images in Cases of Polycystic Ovary Syndrome},
  school = {Universidad Autónoma de Ciudad Juárez},
  year = {2026}
}
```

---

# ⚠️ Disclaimer

This project is intended exclusively for research and educational purposes and is not intended to replace professional medical diagnosis.
