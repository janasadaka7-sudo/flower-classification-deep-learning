# 🌸 Flower Classification Using Deep Learning

## 📌 Project Overview

This project is a Deep Learning image classification system designed to identify the type of flower from an input image.

The project compares several Deep Learning approaches and selects the best-performing model based on validation accuracy.

The final model uses Transfer Learning with MobileNetV2 and achieved a validation accuracy of approximately 89.24%.

---

## 🎯 Project Objective

The main objective of this project is to build an automated system that can classify flower images into their correct categories.

The system receives a flower image as input and predicts:

- The flower type
- The prediction confidence

---

## 📂 Dataset

The project uses the TensorFlow Flower Photos dataset.

Dataset URL:

https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz

The dataset contains five flower classes:

- Daisy
- Dandelion
- Roses
- Sunflowers
- Tulips

The dataset is downloaded and extracted automatically using TensorFlow/Keras.

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

## 🔄 Data Preprocessing

The following preprocessing steps were applied:

1. Downloading and extracting the dataset.
2. Detecting the available flower classes.
3. Counting images for each class.
4. Resizing all images to `128 × 128`.
5. Converting images from BGR to RGB.
6. Shuffling the dataset.
7. Splitting the dataset into training and validation sets.
8. Using stratified splitting to preserve class distribution.
9. Normalizing pixel values from `0–255` to `0–1`.

---

## 🧠 Models Implemented

Four different approaches were implemented and compared.

### 1. MLP (Multi-Layer Perceptron)

The first model was a baseline MLP model.

The input images were flattened and passed through several Dense layers with Dropout.

This model achieved:

**Validation Accuracy: 41.42%**

---

### 2. CNN (Convolutional Neural Network)

A CNN model was implemented because CNNs are more suitable for image classification.

The model contains:

- Convolutional layers
- MaxPooling layers
- Dense layers
- Dropout
- Softmax output layer

Validation Accuracy:

**70.84%**

---

### 3. Improved CNN

The CNN was improved using:

- Data Augmentation
- Random Horizontal Flip
- Random Rotation
- Random Zoom
- Dropout
- Early Stopping

The purpose of these techniques was to reduce overfitting and improve generalization.

Validation Accuracy:

**75.89%**

---

### 4. Transfer Learning with MobileNetV2

The final approach uses the pretrained MobileNetV2 architecture.

The pretrained ImageNet layers were frozen, and new classification layers were added for the flower classes.

The model uses:

- MobileNetV2
- Global Average Pooling
- Dropout
- Dense layer
- Softmax output layer

The model was trained using the Adam optimizer and sparse categorical crossentropy loss.

Validation Accuracy:

**89.24%**

---

## 📊 Model Comparison

| Model | Validation Accuracy |
|---|---:|
| MLP | 41.42% |
| CNN | 70.84% |
| Improved CNN | 75.89% |
| **MobileNetV2** | **89.24%** |

### 🏆 Best Model

The best-performing model is:

**MobileNetV2 with Transfer Learning**

with a validation accuracy of:

**89.24%**

Therefore, MobileNetV2 was selected as the final model.

---

## 📈 Model Evaluation

The models were evaluated using:

- Accuracy
- Validation Loss
- Classification Report
- Confusion Matrix

Training and validation accuracy curves were also plotted to monitor model performance.

---

## 🔍 Flower Prediction

The project allows the user to upload a new flower image using Google Colab.

The uploaded image is:

1. Loaded using OpenCV.
2. Resized to `128 × 128`.
3. Converted from BGR to RGB.
4. Normalized.
5. Passed to the trained model.
6. Classified into one of the five flower categories.

The model returns:

```text
Predicted Flower: tulips
Confidence: 51.5%
Project Workflow
Flower Dataset
      ↓
Data Loading
      ↓
Image Preprocessing
      ↓
Image Resizing
      ↓
Normalization
      ↓
Train / Validation Split
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Comparison
      ↓
Best Model Selection
      ↓
New Image Prediction
🚀 Future Improvements
The project can be improved in the future by
Fine-tuning the pretrained MobileNetV2 layers.
Increasing image resolution.
Using larger and more diverse datasets.
Experimenting with EfficientNet and ResNet.
Applying more advanced data augmentation techniques.
Deploying the model as a web application.
Developing a mobile application for real-time flower recognition.
Adding more flower species to the classification system.
💻 How to Run the Project
1. Open Google Colab

Upload or open the project notebook in Google Colab.

2. Install the Required Libraries

Install the packages listed in requirements.txt if they are not already available.

3. Run the Notebook

Run the cells in order:

Dataset Download
Dataset Exploration
Preprocessing
Model Training
Model Evaluation
Model Comparison
Image Prediction
4. Upload an Image

When the upload cell runs, upload a flower image.

The final model will display the predicted flower type and confidence.

📁 Project Structure
Flower-Classification/
│
├── flower_classification.ipynb
├── README.md
├── requirements.txt
└── flower_cnn_model.h5
🎓 Project Type

Deep Learning / Image Classification

👥 Applications

This project can be used in:

Educational applications
Botanical image recognition
Plant identification systems
Computer Vision projects
Automated flower recognition systems
📌 Conclusion

This project demonstrates the use of Deep Learning and Computer Vision for flower image classification.

Several models were developed and compared, starting with a basic MLP, followed by CNN and Improved CNN models.

Transfer Learning using MobileNetV2 achieved the highest validation accuracy of approximately 89.24%.

Therefore, MobileNetV2 was selected as the final model for the flower classification system.

