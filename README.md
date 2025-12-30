# 🔮 Quantum Machine Learning on the Iris Dataset

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![PennyLane](https://img.shields.io/badge/PennyLane-0.33+-green.svg)](https://pennylane.ai)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yashas396/quantum-ml-iris/blob/main/Quantum_ML_Iris_Complete.ipynb)

A comprehensive exploration of **Quantum Machine Learning** techniques applied to the classic Iris flower classification problem. This project demonstrates multiple QML algorithms, noise simulation, and benchmarking against classical methods.

![Quantum ML Banner](https://img.shields.io/badge/🔬_Quantum-Machine_Learning-purple?style=for-the-badge)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Quantum Methods Implemented](#-quantum-methods-implemented)
- [Installation](#-installation)
- [Usage](#-usage)
- [Results](#-results)
- [Project Structure](#-project-structure)
- [Key Concepts](#-key-concepts)
- [References](#-references)
- [License](#-license)

---

## 🎯 Overview

This project explores whether quantum computers can provide advantages for machine learning tasks. Using the well-known Iris dataset as a benchmark, we implement and compare:

- **4 Quantum ML algorithms** (VQC, QNN, Data Re-uploading, Quantum Kernel SVM)
- **3 Classical baselines** (SVM, Random Forest, Logistic Regression)
- **Noise simulation** to understand real hardware effects
- **Hyperparameter analysis** across circuit depth and qubit count

### Why Iris Dataset?

The Iris dataset is ideal for quantum ML exploration because:
- Small enough to simulate on classical hardware
- Multi-class classification (3 classes)
- Well-understood benchmark for comparison
- 4 features map naturally to 4 qubits

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔄 **Multiple QML Methods** | Compare 4 different quantum approaches |
| 📊 **Comprehensive Visualizations** | Circuit diagrams, training curves, confusion matrices |
| 🔊 **Noise Simulation** | Depolarizing and bit-flip error models |
| ⚡ **Benchmarking** | Performance, training time, circuit complexity |
| 📈 **Hyperparameter Analysis** | Layer depth and qubit sensitivity studies |
| 🎓 **Educational** | Detailed explanations of quantum concepts |

---

## 🔬 Quantum Methods Implemented

### 1. Variational Quantum Classifier (VQC)
- Angle encoding of classical features
- Strongly entangling layers ansatz
- Gradient-based optimization

### 2. Quantum Neural Network (QNN)
- Alternative ansatz architecture
- Multiple optimizer comparison
- Layer depth analysis

### 3. Data Re-uploading Classifier
- Re-encodes data at each layer
- Increased expressibility
- Inspired by classical neural network structure

### 4. Quantum Kernel SVM
- Quantum-computed kernel matrix
- Classical SVM with quantum kernel
- Explores quantum feature spaces

---

## 🚀 Installation

### Option 1: Google Colab (Recommended)
Click the "Open in Colab" badge above - no installation needed!

### Option 2: Local Installation

```bash
# Clone the repository
git clone https://github.com/yashas396/quantum-ml-iris.git
cd quantum-ml-iris

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook Quantum_ML_Iris_Complete.ipynb
```

---

## 📖 Usage

1. **Open the notebook** in Jupyter or Google Colab
2. **Run all cells** sequentially (some cells may take a few minutes)
3. **Explore the results** - all visualizations are generated inline
4. **Experiment** by modifying hyperparameters

### Quick Start
```python
# The notebook handles everything, but if you want to use the code separately:
import pennylane as qml
from pennylane import numpy as np

# Create a quantum device
dev = qml.device("default.qubit", wires=4)

# Your quantum circuit here...
```

---

## 📊 Results

### Accuracy Comparison

| Method | Accuracy | Type |
|--------|----------|------|
| Variational Quantum Classifier | ~95% | Quantum |
| Quantum Neural Network | ~93% | Quantum |
| Data Re-uploading | ~94% | Quantum |
| Quantum Kernel SVM | ~96% | Quantum |
| Classical SVM (RBF) | ~97% | Classical |
| Random Forest | ~95% | Classical |

> **Note**: For this small dataset, classical methods perform comparably. Quantum advantage is expected for larger, more complex datasets.

### Key Findings

1. **Quantum methods achieve competitive accuracy** with classical approaches
2. **Noise significantly impacts performance** - error mitigation is crucial
3. **Circuit depth has diminishing returns** after 3-4 layers
4. **Quantum kernels** show promise for capturing complex feature relationships

---

## 📁 Project Structure

```
quantum-ml-iris/
├── Quantum_ML_Iris_Complete.ipynb  # Main comprehensive notebook
├── README.md                        # This file
├── requirements.txt                 # Python dependencies
└── LICENSE                          # MIT License
```

---

## 🎓 Key Concepts

### Quantum Data Encoding
- **Angle Encoding**: Features → Rotation angles (RX, RY, RZ gates)
- **Amplitude Encoding**: Features → Quantum state amplitudes
- **IQP Encoding**: Diagonal gates with feature interactions

### Variational Circuits
Parameterized quantum gates whose parameters are optimized classically:
```
|0⟩ ─ H ─ RY(θ₁) ─ CNOT ─ RZ(θ₂) ─ ⟨Z⟩
```

### Quantum Kernels
Use quantum computers to compute similarity between data points in a high-dimensional Hilbert space.

---

## 📚 References

1. **PennyLane Documentation**: [pennylane.ai/qml](https://pennylane.ai/qml/)
2. **Variational Quantum Classifier**: [arXiv:1804.00633](https://arxiv.org/abs/1804.00633)
3. **Quantum Kernel Methods**: [Nature 567, 209–212 (2019)](https://www.nature.com/articles/s41586-019-0980-2)
4. **Data Re-uploading**: [arXiv:1907.02085](https://arxiv.org/abs/1907.02085)
5. **QML Review**: [arXiv:2101.11037](https://arxiv.org/abs/2101.11037)

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Open issues for bugs or suggestions
- Submit pull requests with improvements
- Share your results and experiments

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [PennyLane](https://pennylane.ai/) team for the excellent quantum ML library
- [Xanadu](https://www.xanadu.ai/) for quantum computing resources
- The quantum computing community for research and inspiration

---

<p align="center">
  <b>⚛️ Happy Quantum Computing! ⚛️</b>
</p>
