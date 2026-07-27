# 🦋 Butterfly Image Segmentation with U-Net

A deep learning project for butterfly image segmentation using the U-Net architecture. This project implements a complete pipeline for loading the Leeds Butterfly Dataset, training a U-Net model, and performing image segmentation to isolate butterflies from their backgrounds.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Dataset](#-dataset)
- [Technology Stack](#-technology-stack)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Data Preparation](#-data-preparation)
- [Model Architecture](#-model-architecture)
- [Training](#-training)
- [Evaluation Metrics](#-evaluation-metrics)
- [Results](#-results)
- [Inference](#-inference)
- [Performance](#-performance)
- [Model Saving](#-model-saving)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

This project leverages the U-Net architecture to perform semantic segmentation on butterfly images. The model is trained to accurately segment butterflies from their backgrounds, which has applications in biological research, species identification, and computer vision.

---

## ✨ Features

- **End-to-end Pipeline**: Complete workflow from data loading to model inference
- **U-Net Architecture**: State-of-the-art segmentation model with skip connections
- **Google Colab Support**: Optimized for running in Colab environment
- **Performance Metrics**: Dice coefficient and Mean IoU for evaluation
- **Visualization**: Comprehensive visualization of predictions and segmentations
- **Model Checkpointing**: Automatic saving of best model during training
- **Customizable**: Easy to modify hyperparameters and architecture

---

## 📊 Dataset

### Leeds Butterfly Dataset
- **Source**: [Kaggle - Butterfly Dataset](https://www.kaggle.com/datasets/veeralakrishna/butterfly-dataset)
- **Images**: 832 images with corresponding masks
- **Resolution**: Variable (resized to 256x256 for training)
- **Content**: Butterfly images with segmentation masks
- **License**: Community Data License Agreement - Permissive - Version 1.0

### Dataset Structure
leedsbutterfly/

├── images/ # Original butterfly images (832 files)

├── segmentations/ # Corresponding segmentation masks (832 files)

└── descriptions/ # Text descriptions of each image


---

## 🛠️ Technology Stack

| Category | Technologies |
|----------|--------------|
| **Language** | Python 3.7+ |
| **Deep Learning** | TensorFlow, Keras |
| **Computer Vision** | OpenCV, PIL |
| **Numerical Computing** | NumPy |
| **Visualization** | Matplotlib |
| **Environment** | Google Colab, Jupyter Notebook |

---

## 📦 Installation

### Option 1: Google Colab (Recommended)

```python
# Clone the repository
!git clone <repository-url>
cd <project-directory>

# Install dependencies
!pip install tensorflow opencv-python pillow matplotlib numpy scikit-learn
```

## Project structure

butterfly-segmentation/

├── README.md                         # Project documentation

├── requirements.txt                   # Python dependencies

├── butterfly_segmentation.ipynb       # Main Jupyter notebook

├── unet_model_best.keras             # Best saved model

├── final_UNET_Butterfly_Segmentation.keras  # Final trained model

├── data/

│   └── leedsbutterfly/               # Dataset directory

│       ├── images/                   # 832 butterfly images

│       ├── segmentations/            # 832 segmentation masks

│       └── descriptions/             # 10 text description files

└── utils/
    └── visualization.py              # Utility functions for visualization


## Architecture Details
Input: (256, 256, 3)

Filters: Starting from 16, doubling at each level

Layers: 5 encoder blocks, 4 decoder blocks

Activation: ReLU (hidden), Sigmoid (output)

Dropout Rate: 0.07

Batch Normalization: Yes

## Model Summary
Total Parameters: 2,164,593

Trainable Parameters: 2,161,649

Non-trainable Parameters: 2,944

Keras :https://drive.google.com/drive/u/0/folders/1WTdcym0SdNCdLwV3N_be2xlN1d8GjG6U
