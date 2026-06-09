# 🧬 Quantum Machine Learning for PCOS Ultrasound Classification using QCNN

<p align="center">
  <img src="assets/banner_qcnn.png" alt="QCNN Banner" width="100%">
</p>

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![TensorFlow Quantum](https://img.shields.io/badge/TensorFlow%20Quantum-QML-purple)
![Cirq](https://img.shields.io/badge/Cirq-Quantum-red)
![Research](https://img.shields.io/badge/Research-QCNN-green)

### Master's Thesis Project – Universidad Autónoma de Ciudad Juárez

</div>

---

# 🌟 Highlights

- Hybrid Quantum-Classical QCNN Architecture
- Medical Image Classification (PCOS vs Non-PCOS)
- 2,000 Ultrasound Images
- 8-Qubit Quantum Circuit
- Accuracy: **87.33%**
- AUC-ROC: **0.9318**
- TensorFlow Quantum + Cirq

---

# 🏗️ Project Workflow

```mermaid
flowchart LR
A[Ultrasound Images] --> B[Data Cleaning]
B --> C[Preprocessing]
C --> D[PCA]
D --> E[Quantum Encoding]
E --> F[QCNN]
F --> G[Pauli-Z Readout]
G --> H[Dense Layer]
H --> I[Prediction]
```

---

# 📸 Results

## QCNN Architecture

![QCNN Circuit](assets/qcnn_circuit.png)

## Confusion Matrix

![Confusion Matrix](results/confusion_matrix.png)

## ROC Curve

![ROC Curve](results/roc_curve.png)

## Training History

| Accuracy | Loss |
|-----------|------|
| ![](results/accuracy.png) | ![](results/loss.png) |

---

# 📊 Performance

| Metric | Value |
|----------|----------:|
| Accuracy | 87.33% |
| AUC-ROC | 0.9318 |
| PCOS Precision | 90.58% |
| PCOS Recall | 83.33% |
| Non-PCOS Precision | 84.57% |
| Non-PCOS Recall | 91.33% |

---

# 📂 Repository Structure

```text
.
├── assets/
│   ├── banner_qcnn.png
│   └── qcnn_circuit.png
├── data/
├── notebooks/
├── src/
├── results/
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── accuracy.png
│   └── loss.png
├── README.md
└── requirements.txt
```

---

# 👨‍💻 Author

Jonathan Adrian Herrera Castro

Master's Degree in Artificial Intelligence and Data Analytics

Universidad Autónoma de Ciudad Juárez (UACJ)

---

# 📚 Citation

```bibtex
@mastersthesis{herrera2026qcnn,
  author={Jonathan Adrian Herrera Castro},
  title={Quantum Machine Learning for the Classification of Ultrasound Images in Cases of Polycystic Ovary Syndrome},
  school={Universidad Autónoma de Ciudad Juárez},
  year={2026}
}
```
