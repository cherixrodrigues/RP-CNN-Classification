# RP-CNN-Classification

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Academic%20Project-green)](.)

> Deep Learning pipeline for **Retinitis Pigmentosa (RP)** gene group classification using Convolutional Neural Networks and Transfer Learning with ResNet architectures.

---

## Overview

Retinitis Pigmentosa (RP) is a heterogeneous group of inherited retinal dystrophies caused by mutations in over 80 genes. This project develops a CNN-based classification pipeline to distinguish between **5 gene groups** — both syndromic and non-syndromic — from retinal imaging data, leveraging Transfer Learning with ResNet models pre-trained on ImageNet.

### Key Features

- **Transfer Learning** with ResNet (ResNet-18 / ResNet-50) via PyTorch & torchvision
- **5-class classification** covering syndromic and non-syndromic RP gene groups
- **K-Fold Cross-Validation** for robust model evaluation across data splits
- **Detailed metrics**: Classification Report, Confusion Matrix, per-class accuracy
- **Reproducible** training pipeline with configurable hyperparameters

---

## Gene Groups

| Group | Type | Description |
|-------|------|-------------|
| Group 1 | Non-syndromic | Autosomal dominant RP genes |
| Group 2 | Non-syndromic | Autosomal recessive RP genes |
| Group 3 | Non-syndromic | X-linked RP genes |
| Group 4 | Syndromic | Usher syndrome genes |
| Group 5 | Syndromic | Bardet-Biedl syndrome genes |

---

## Project Structure

```
RP-CNN-Classification/
│
├── notebooks/                  # Jupyter notebooks for experiments
│   └── .gitkeep
│
├── docs/                       # Documentation and figures
│   └── .gitkeep
│
├── .github/
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md
│       └── feature_request.md
│
├── README.md
├── LICENSE
├── .gitignore
└── requirements.txt
```

---

## Installation

### Prerequisites

- Python 3.8+
- CUDA-compatible GPU (recommended)

### Setup

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/RP-CNN-Classification.git
cd RP-CNN-Classification

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # Linux/macOS
venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Usage

### Training

Open and run the main training notebook:

```bash
jupyter notebook notebooks/
```

### Cross-Validation

The pipeline uses stratified K-Fold cross-validation. Each fold trains a ResNet model from scratch (with frozen/unfrozen backbone options) and evaluates on the held-out fold.

### Evaluation Metrics

After training, the pipeline produces:

- **Confusion Matrix** — per-fold and aggregated
- **Classification Report** — precision, recall, F1-score per gene group
- **Accuracy curves** — training vs. validation per epoch

---

## Results

> Results section to be updated after final experiments.

| Model | Folds | Mean Accuracy | Mean F1 (macro) |
|-------|-------|---------------|-----------------|
| ResNet-18 | 5 | — | — |
| ResNet-50 | 5 | — | — |

---

## Dependencies

See [`requirements.txt`](requirements.txt) for the full list. Core libraries:

- [PyTorch](https://pytorch.org/) — model training and inference
- [torchvision](https://pytorch.org/vision/) — ResNet models and image transforms
- [scikit-learn](https://scikit-learn.org/) — cross-validation and metrics
- [Pillow](https://python-pillow.org/) — image loading
- [matplotlib](https://matplotlib.org/) / [seaborn](https://seaborn.pydata.org/) — visualization

---

## Academic Context

This project was developed as part of a **Deep Learning** coursework focused on medical image analysis and genetic classification of retinal diseases.

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
