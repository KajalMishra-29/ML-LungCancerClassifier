# 🧠 ML-LungCancerClassifier
This project aims to develop a machine learning model for the classification of lung cancer images into three categories: benign cases, malignant cases, and normal cases. Assist in early and accurate detection of lung cancer using deep learning.

This project includes two model architectures:
- Custom CNN Model: Lightweight convolutional architecture built from scratch for image classification.
- ResNet-based Model: A deeper and more powerful feature extractor using ResNet50.Helps improve accuracy and generalization.

Both models are evaluated on the same dataset using:

# 📂 Dataset
Sourced from Kaggle: `IQ-OTH/NCCD Lung Cancer` Dataset
It contains labeled CT images across the three classes.


## 🔁 Project Pipeline
- **Data Preprocessing**
  - image resizing and normalization
  - Label encoding
  - Dataset split : `70%` Training | `15%` Validation | `15%` Testing
- **Model Architectures**
    - Custom `Concolutional Neural Network` (CNN)
    - `ResNet50` (pre-trained on ImageNet, fine-tuned on this dataset)
- **Model Training**
    - Compiled with `categorical_crossentropy` loss and `Adam` optimizer
    - Early stopping & ReduceLR
- **Model Evaluation**
    - Accuracy & Loss Curves (train vs val)
    - Classification Report: Accuracy, Precision, Recall, F1-score
    - Confusion Matrix
    - Multi-class ROC-AUC Curve
