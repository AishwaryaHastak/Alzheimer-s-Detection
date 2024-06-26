# NeuroDetect: MRI‑Based Alzheimer’s Disease Detection using DNN

## Overview
Training a Deep Neural Network to classify images of brain MRI scans to identify Dementia and Non-Dementia Patients.

The goal of this project is to use a simpler architecture with fewer parameters and still achieve good accuracy. The approach of this project is more data-centric, where we keep the model architecture constant, and focus more on augmenting the data and fine-tuning the hyperparameters.

The dataset is sourced from Kaggle and can be found at [Alzheimer's Dataset](https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images)

## Dealing with imbalanced classes

The dataset contains images for 4 classes:
1. Mild Demented
2. Moderate Demented
3. Non Demented
4. Very Mild Demented
   
The class distribution is as follows:

<img src="https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/d8d2acd0-2164-4d52-8f7d-981b1aca6ea1" width="500">


### Techniques to handle class imbalance
The dataset exhibits significant class imbalance, a common occurrence in medical imaging data, where instances of individuals without a certain condition often outnumber those with the condition. To address this issue, I employed and compared two data augmentation techniques to boost the number of instances in underrepresented classes. First, I utilized SMOTE (Synthetic Minority Over-sampling Technique), which equalized the instance counts across all classes. Second, I manually augmented the data for each class, ensuring that while each label had sufficient instances for training, the overall distribution of data remained consistent. This approach maintained the relative differences in instance counts between labels, preserving the general distribution of the dataset. The resulting distributions are illustrated below:

<img src="https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/b4156ce0-3089-4293-8d8c-a9865f182f43" width="500">



### So what does it mean? 
The model tends to perform better when the class distribution closely mirrors real-life scenarios. Instead of equalizing instance counts across all classes, the goal was to ensure each class had sufficient training examples while retaining the overall distribution. This approach offers a better representation of real-world conditions, enhancing the model's performance.


## Model 

Several models developed on this dataset leveraged pre-trained architectures such as RESNET [1], VGG, and others, achieving remarkable accuracies nearing 94%. Conversely, a different approach employed a more straightforward Convolutional Neural Network model, yielding a validation set accuracy of approximately 80% [2]. This project endeavors to craft a simplified DNN model, boasting fewer parameters than expansive architectures like RESNET, all while upholding high accuracy standards.

## References

[1] [Alzheimer's Detection using DL](https://www.kaggle.com/code/mihirbhatkar/alzheimer-s-detection-using-dl)

[2] [Class Prediction with PyTorch](https://www.kaggle.com/code/natsu18/class-prediction-pytorch)

