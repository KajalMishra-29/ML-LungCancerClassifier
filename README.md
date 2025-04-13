# 🧠 ML-LungCancerClassifier
This project aims to develop a deep learning-based classifier for lung CT images, categorizing them into three clinical labels:
- `Benign`
- `Malignant`
- `Normal`
The goal is early detection and diagnosis of lung cancer using deep learning models.

# 🏗️ Model Architectures Used:
1. Custom CNN Model
   - Built from scratch with Tensorflow/Keras.
   - Lightweight and fast.
   - Achieved 96.67% accuracy on test set.
   - ## Architectural Flow
      ```
         Conv2D (64, 3x3) → ReLU → MaxPooling2D (2x2)
         Conv2D (64, 3x3) → ReLU → MaxPooling2D (2x2)
         Flatten → Dense(16) → Dense(3, Softmax)
      ```
2. ResNet-based Model
   - Transfer learning using pretrained ResNet50 (ImageNet weights).
   - Fine-tuned on your dataset.
   - Achieved  95.76% accuracy on the test set.

# 📊 Dataset Details:          
- Sourced from Kaggle: `IQ-OTH/NCCD Lung Cancer` Dataset          
- Contains CT scan images classified into:
   - `0` – Normal
   - `1` – Malignant
   - `2` – Benign            

# 🔁 Project Pipeline
- **Data Preprocessing**
  - image resizing and normalization
  - Label encoding : `1`(Malignant) , `2`(Benign), `0`(Normal) 
  - Dataset split : `70%` Training | `15%` Validation | `15%` Testing
- **Model Architectures**
    - Custom `Concolutional Neural Network` (CNN)
    - `ResNet50` (pre-trained on ImageNet, fine-tuned on this dataset)
- **Model Training**
   - Loss function: `Categorical Crossentropy`
   - Optimizer: `Adam`
   - Callbacks: EarlyStopping, ReduceLROnPlateau
- **Model Evaluation**
    Accuracy & Loss plots (Training vs Validation)
   - Classification Report:
      - Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix
   - Multi-class ROC-AUC Curve
 
  ![image](https://github.com/user-attachments/assets/ae4bb760-23fd-4780-9b41-a3b118e374eb)

# 💡 Future Enhancements
- Grad-CAM visualization for interpretability
- Deployment as a Streamlit/Flask app
- Add support for more complex architectures (EfficientNet, Vision Transformers)
- Explore ensemble methods to boost performance

