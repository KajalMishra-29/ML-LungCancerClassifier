# 🧠 ML-LungCancerClassifier
This project aims to develop a machine learning model for the classification of CT images into three categories: `benign`, `malignant`, and `normal` cases.This aids in the early detection and diagnosis of lung cancer using deep learning models.

# 🏗️ Model Architectures Used:
1. Custom CNN Model
   - Built from scratch with Tensorflow/Keras.
   - Lightweight and fast.
   - Achieved 96.67% accuracy on test set.
   - ## Architectural Flow
      - 2 Convolutional Layers each with:
         - `64 filters`, `3x3` kernels
         - Followed by **ReLU activation**
         - Followed by 2x2 **MaxPooling** (downsampling feature maps)
      - Flatten: Converts 2D feature maps into 1D
      - Dense(16): Fully connected layer
      - Dense(3) with Softmax: Output for 3-class classification
      - ```
         Conv2D → ReLU → MaxPooling ×2
         Flatten → Dense(16)
         Dense(3) → Softmax
        ```
2. ResNet-based Model
   - Transfer learning using pretrained ResNet50 (ImageNet weights).
   - Fine-tuned on your dataset.
   - Achieved  95.76% accuracy on the test set.

# 📊 Dataset Details:          
- Sourced from Kaggle: `IQ-OTH/NCCD Lung Cancer` Dataset          
- 3-class classification: Malignant, Benign, Normal.             

# 🔁 Project Pipeline
- **Data Preprocessing**
  - image resizing and normalization
  - Label encoding : `1 Malignant` , `2 Benign`, `0 Normal` 
  - Dataset split : `70%` Training | `15%` Validation | `15%` Testing
- **Model Architectures**
    - Custom `Concolutional Neural Network` (CNN)
    - `ResNet50` (pre-trained on ImageNet, fine-tuned on this dataset)
- **Model Training**
    - Compiled with `categorical_crossentropy` loss and `Adam` optimizer
    - Callbacks such as early stopping & ReduceLR
- **Model Evaluation**
    - Accuracy & Loss Curves (train vs val)
    - Classification Report: Accuracy, Precision, Recall, F1-score
    - Confusion Matrix
    - Multi-class ROC-AUC Curve
