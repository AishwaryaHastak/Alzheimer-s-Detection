# NeuroDetect: MRI‑Based Alzheimer’s Disease Detection using DNN

## 🧠 Overview
Training a Deep Neural Network (DNN) to classify brain MRI scans for detecting Dementia versus Non-Dementia patients. This project aims to use a simpler architecture with fewer parameters while still achieving good accuracy. We focus on a data-centric approach, emphasizing data augmentation and fine-tuning hyperparameters rather than complex model architectures.

The dataset is sourced from Kaggle and can be found at [Alzheimer's Dataset](https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images)

## 🎯 Objective
The main objective of this project was not to create a model with the highest state-of-the-art (SOTA) accuracy but to understand how data affects model performance. By defining a simple CNN model and keeping it fixed, we focused on using data augmentation techniques and hyperparameter tuning to improve accuracy.

## 💡 Skills
- PyTorch
- Python
- MLFlow
- Data Augmentation
- Hyperparameter Tuning

## ⚖️ Dealing with imbalanced classes

The dataset contains images for 4 classes:
1. Mild Demented
2. Moderate Demented
3. Non Demented
4. Very Mild Demented
   
The class distribution is as follows:

<img src="https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/d8d2acd0-2164-4d52-8f7d-981b1aca6ea1" width="500">


### Techniques to handle class imbalance
The dataset exhibits significant class imbalance. To address this, I employed and compared two data augmentation techniques:

1. **SMOTE** (Synthetic Minority Over-sampling Technique): Equalized the instance counts across all classes.

2.** Manual Augmentation**: Boosted the number of instances in underrepresented classes while retaining the overall class distribution. This approach maintained the relative differences in instance counts, offering a better representation of real-world conditions

**Result**: The model performs better when the class distribution closely mirrors real-life scenarios, providing a more accurate reflection of actual conditions.

<img src="https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/b4156ce0-3089-4293-8d8c-a9865f182f43" width="500">

##🛠️ Model 

Several models developed on this dataset leveraged pre-trained architectures such as RESNET [1], VGG, and others, achieving remarkable accuracies nearing 94%. Conversely, a different approach employed a more straightforward Convolutional Neural Network model, yielding a validation set accuracy of approximately 80% [2]. This project endeavors to craft a simplified DNN model, boasting fewer parameters than expansive architectures like RESNET, all while upholding high accuracy standards.

## References

[1] [Alzheimer's Detection using DL](https://www.kaggle.com/code/mihirbhatkar/alzheimer-s-detection-using-dl)

[2] [Class Prediction with PyTorch](https://www.kaggle.com/code/natsu18/class-prediction-pytorch)

