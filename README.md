# Deep Learning Assignment 2 — CIFAR-10 Image Classification

A deep learning project focused on CIFAR-10 image classification using a lightweight Inception-style Convolutional Neural Network (CNN), data augmentation, regularization, and model evaluation with PyTorch.

## 📌 Project Overview

This project investigates image classification performance when training data is limited to only **500 images** from the CIFAR-10 dataset. It explores different augmentation and regularization strategies to improve generalization and analyzes model errors on clean and corrupted images.

## 🎯 Objectives

- Build a lightweight CNN with an Inception-style module.
- Train and evaluate the model using a limited CIFAR-10 training subset.
- Compare data augmentation and regularization techniques.
- Perform an ablation study across multiple random seeds.
- Analyze per-class accuracy and common classification errors.
- Evaluate Test-Time Augmentation (TTA).

## 🧠 Model Architecture

The project uses a custom Inception-style CNN with parallel feature-extraction branches, including:

- **1×1 convolution**
- **3×3 convolution**
- **5×5 convolution**
- **Pooling branch**

The model contains approximately **13,874 trainable parameters**, remaining below the assignment limit of one million parameters.

## 📊 Dataset and Experimental Setup

- **Dataset:** CIFAR-10
- **Training subset:** 400 images (40 per class)
- **Validation subset:** 100 images (10 per class)
- **Classes:** 10
- **Framework:** PyTorch
- **Platform:** Google Colab

The official CIFAR-10 test set is used for clean-test evaluation. A self-generated Gaussian-noise corruption is also used as a proxy for evaluating robustness to corrupted inputs.

## 🔬 Experiments

The notebook covers the following parts:

- **Part A — Baseline Model:** Training without data augmentation and evaluating model performance.
- **Part B — Data Augmentation:** Exploring geometric and photometric transformations.
- **Part C — Regularization:** Evaluating label smoothing and Random Erasing.
- **Part D — Ablation Study:** Comparing different augmentation and regularization configurations across random seeds.
- **Part E — Error Analysis:** Examining per-class accuracy, confusion patterns, misclassified images, and corruption robustness.
- **Part F — Test-Time Augmentation:** Averaging predictions from original and horizontally flipped images.

## 📈 Selected Results

| Experiment | Result |
|---|---:|
| Baseline validation accuracy | 35.00% |
| Baseline clean-test accuracy | 37.12% |
| Selected model clean-test accuracy | 36.29% |
| Best reported mean validation accuracy | 38.67% ± 4.93% |
| TTA accuracy | 36.31% |
| TTA improvement | +0.02 percentage points |

The best reported mean validation accuracy was achieved by **Photometric Augmentation + Label Smoothing** across three random seeds. Results may vary because of the small training and validation subsets.

**Note:** Gaussian-noise evaluation is a self-generated proxy, not the official shifted-test benchmark.

## 🛠️ Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

## 🚀 How to Run

1. Open the notebook `DL_ASS02_23F_0640.ipynb` in Google Colab.
2. Ensure the runtime has the required Python libraries installed.
3. Run the notebook cells in sequence.
4. Allow the dataset to download and the experiments to execute.
5. Review the accuracy results, plots, confusion matrix, and error analysis.

A GPU runtime is recommended to reduce training time.

## 📁 Repository Structure

```text
DLP-Assignment-2-CIFAR10/
├── DL_ASS02_23F_0640.ipynb
└── README.md
```

## 👨‍🎓 Author

**Muhammad Luqman**  
Student ID: 23F-0640

## 📚 Acknowledgment

This project was completed as part of a Deep Learning course assignment using the CIFAR-10 dataset.

---

*This repository is intended for educational purposes and experimentation with image classification under limited-data conditions.*
