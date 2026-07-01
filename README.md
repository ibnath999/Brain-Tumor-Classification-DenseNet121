# Brain Tumor Classification using DenseNet121

## Overview

This project presents a deep learning framework for multiclass brain tumor classification using MRI images. The model employs a pretrained DenseNet121 backbone with transfer learning and fine-tuning to accurately classify brain MRI scans into four categories.

## Features

- DenseNet121 (ImageNet Pretrained)
- Transfer Learning
- Fine-Tuning
- Batch Normalization
- Dropout Regularization
- Label Smoothing
- Warmup + Cosine Learning Rate Scheduler
- Early Stopping
- Mixed Precision Training
- Grad-CAM Explainability
- ROC Curve Analysis
- Confusion Matrix

---

## Dataset

**Source**
https://drive.google.com/file/d/1OPUSnue5Kj0jjgOnSmE4Cbzu9jYztZJG/view?usp=drive_link


### Classes

- Glioma
- Meningioma
- Pituitary Tumor
- No Tumor

### Input Size

224 × 224 × 3

---

## Model Architecture

```
Input Image (224×224×3)
        │
DenseNet121 (ImageNet)
        │
Global Average Pooling
        │
Batch Normalization
        │
Dense Layer
        │
Dropout
        │
Dense Layer
        │
Softmax (4 Classes)
```

---

## Training Configuration

| Parameter | Value |
|-----------|--------|
| Backbone | DenseNet121 |
| Optimizer | Adam |
| Image Size | 224×224 |
| Batch Size | 32 |
| Loss | Categorical Crossentropy |
| Label Smoothing | Enabled |
| Learning Rate Scheduler | Warmup + Cosine Decay |
| Mixed Precision | Enabled |
| Fine-Tuning | Enabled |

---

## Evaluation Metrics

The trained model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Cohen's Kappa
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix
- ROC Curve
- Grad-CAM Visualization

---

## Results

The DenseNet121 model achieved excellent classification performance on the four-class brain MRI dataset with strong generalization capability.

---


## Usage

Open and run the notebook:

```bash
jupyter notebook densenet.ipynb
```

---

## Future Work

- Compare DenseNet121 with EfficientNet and ConvNeXt.
- Improve explainability using Score-CAM and Grad-CAM++.
- Evaluate on additional external MRI datasets.

---

## Author

**AKILA IBNATH**



Research Interests:
- Deep Learning
- Medical Image Analysis
- Computer Vision
- Explainable AI
