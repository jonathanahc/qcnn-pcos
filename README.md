# Quantum Convolutional Neural Network for Ultrasound Image Classification in PCOS

> **Hybrid Quantum-Classical Machine Learning applied to medical imaging**
> Master's research project — Universidad Autónoma de Ciudad Juárez (UACJ), 2025–present

---

## What this project does

Polycystic Ovary Syndrome (PCOS) is one of the most common hormonal disorders in women of reproductive age, yet its diagnosis relies heavily on manual interpretation of ultrasound images — a process that is slow, subjective, and dependent on specialist availability.

This project trains a **Quantum Convolutional Neural Network (QCNN)** to automatically classify ultrasound images as PCOS-positive or PCOS-negative. It combines classical preprocessing and dimensionality reduction with quantum circuits to explore whether quantum computing can bring meaningful advantages to medical image classification.

**Bottom line:** The model achieves **87.33% accuracy** and an **AUC of 0.9318** on held-out test data.

---

## Results

| Metric | Value |
|---|---|
| Accuracy | **87.33%** |
| AUC-ROC | **0.9318** |
| Model type | Hybrid QCNN (classical + quantum) |
| Task | Binary classification (PCOS / No PCOS) |

> Confusion matrix, ROC curve, and training history plots are available in the `/results` folder.

---

## How it works

The pipeline has four stages:

```
Ultrasound images
       ↓
Preprocessing (resize, normalize, augment)
       ↓
Dimensionality reduction (PCA → n quantum features)
       ↓
Quantum encoding (amplitude / angle encoding)
       ↓
Quantum Convolutional Neural Network (TensorFlow Quantum + Cirq)
       ↓
Binary classification output
```

**Classical stage:** Images are preprocessed using standard computer vision techniques (normalization, resizing, data augmentation). PCA reduces the feature space to a size compatible with the quantum circuit.

**Quantum stage:** Reduced features are encoded into quantum states. A parameterized quantum circuit — the QCNN — applies convolutional and pooling layers in Hilbert space, trained via gradient descent on expectation values.

**Why quantum?** Quantum circuits can represent certain feature correlations more compactly than classical networks of equivalent depth. This project tests that hypothesis on a real medical dataset.

---

## Tech stack

| Layer | Tools |
|---|---|
| Quantum framework | TensorFlow Quantum, Cirq |
| Classical ML | Scikit-learn, Keras |
| Data processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Dimensionality reduction | PCA (scikit-learn) |
| Environment | Python 3.10, Google Colab / local |

---

## Project structure

```
qcnn-pcos/
├── data/
│   └── README.md              # Dataset description and access instructions
├── notebooks/
│   ├── 01_preprocessing.ipynb # Image loading, normalization, augmentation
│   ├── 02_pca_encoding.ipynb  # PCA + quantum feature encoding
│   ├── 03_qcnn_training.ipynb # Circuit design, training loop, evaluation
│   └── 04_results.ipynb       # Metrics, plots, confusion matrix
├── src/
│   ├── preprocessing.py       # Reusable preprocessing functions
│   ├── encoding.py            # Quantum data encoding utilities
│   ├── model.py               # QCNN circuit and model definition
│   └── evaluate.py            # Evaluation metrics and visualization
├── results/
│   ├── roc_curve.png
│   ├── confusion_matrix.png
│   └── training_history.png
├── requirements.txt
└── README.md
```

---

## Getting started

### Requirements

```bash
pip install tensorflow tensorflow-quantum cirq scikit-learn pandas numpy matplotlib seaborn
```

Or install all dependencies at once:

```bash
pip install -r requirements.txt
```

### Run the full pipeline

1. Clone the repository:
```bash
git clone https://github.com/jonathanadrianhc/qcnn-pcos.git
cd qcnn-pcos
```

2. Open the notebooks in order (`01` → `04`) in Jupyter or Google Colab.

3. For a quick evaluation run using pretrained weights:
```bash
python src/evaluate.py --model_path results/model_weights.h5
```

### Dataset

> The dataset used in this project consists of labeled ultrasound images. Due to privacy and licensing constraints, raw images are not included in this repository. A description of the dataset characteristics and preprocessing steps is provided in `data/README.md`.
>
> *If you are a researcher interested in reproducing these results, feel free to open an issue.*

---

## Academic context

This project is the core of my Master's thesis in Artificial Intelligence and Data Analytics at UACJ. It was presented at the **II Cumbre Nacional de Posgrados (May 2026)**, where it received recognition from the Instituto de Ingeniería y Tecnología.

Related publication (different architecture, same research line):

> Herrera-Castro, J.A. et al. *"Acquisition, Processing, and Visualization of Meteorological Data in Real-Time using Apache Flink."* In: *Data Analytics & Computational Intelligence: Novel Models, Algorithms and Applications.* Springer, 2023.

---

## Author

**Jonathan Adrian Herrera Castro**
M.Sc. candidate — Artificial Intelligence & Data Analytics, UACJ
Ciudad Juárez, Chihuahua, México

[![LinkedIn](https://img.shields.io/badge/LinkedIn-jonathan--adrian--herrera--castro-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/jonathan-adrian-herrera-castro)
[![Email](https://img.shields.io/badge/Email-jonathanadrianhc%40hotmail.com-EA4335?style=flat&logo=gmail)](mailto:jonathanadrianhc@hotmail.com)

---

## License

This project is licensed under the MIT License. See `LICENSE` for details.

---

*Last updated: June 2026*
