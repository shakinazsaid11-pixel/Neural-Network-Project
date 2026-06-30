# Neural-Network-Project

# 🩸 Blood Cell Image Classification: CNN vs FFNN

A deep learning project that designs, trains, and compares two neural network architectures — a **Feedforward Neural Network (FFNN)** and a **Convolutional Neural Network (CNN)** — on a multi-class blood cell image dataset.

## 📌 Overview

This project explores the fundamental difference between treating images as flat vectors (FFNN) versus preserving their spatial structure (CNN). Both models are trained from scratch using PyTorch, then rigorously evaluated on the same held-out test set.

## 🗂️ Dataset

A blood cell image dataset with **8 classes**, split into train / validation / test sets using **stratified sampling** to preserve class balance.

## 🔬 What's Inside

- **Exploratory Data Analysis (EDA)** — class distribution, image dimensions, sample grids, and data quality checks
- **Preprocessing Pipeline** — resizing to 64×64, normalization, and data augmentation (horizontal flip, rotation) for training
- **FFNN Baseline** — flattens 3×64×64 images into vectors, trained with dropout and L2 regularization
- **CNN Model** — 4 convolutional blocks with BatchNorm, ReLU, and MaxPooling, followed by a fully connected classifier
- **Training Utilities** — early stopping, learning curve plotting, and reproducibility via fixed seeds
- **Optimization Trials** — configurable trial function to test different learning rates, dropout rates, and depths
- **Final Comparison** — accuracy, macro F1-score, training time, average epoch time, and inference speed side by side

## 🧠 Key Concepts Demonstrated

- Spatial feature extraction with convolutional layers vs. pixel-level pattern learning with dense layers
- Regularization techniques: Dropout, L2 weight decay, Batch Normalization
- Overfitting / underfitting diagnosis via learning curves
- Why **macro F1-score** matters alongside accuracy for potentially imbalanced classes

## 🛠️ Tech Stack

`Python` · `PyTorch` · `torchvision` · `scikit-learn` · `NumPy` · `Pandas` · `Matplotlib` · `Pillow`

## 🚀 How to Run

1. Place `archive.zip` (the blood cells dataset) in this link:https://www.kaggle.
com/datasets/uncles
amulus/blood-cellsimage-dataset/data
2. Install dependencies: `pip install torch torchvision scikit-learn matplotlib pillow pandas`
3. Run all cells top to bottom

## 📊 Results

The CNN is expected to outperform the FFNN in accuracy and macro F1 because it learns local visual patterns like cell edges and textures, while the FFNN discards spatial information by flattening the image.

