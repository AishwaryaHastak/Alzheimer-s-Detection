# Alzheimer-s-Detection

## Overview
Training a Deep Neural Network to classify images of brain MRI scans to identify Dementia and Non-Dementia Patients.

The dataset is sourced from Kaggle and can be found at: Alzheimer's Dataset

## Dealing with imbalanced classes

The dataset contains images for 4 classes:

1. Mild Demented
2. Moderate Demented
3. Non Demented
4. Very Mild Demented
The class distribution is as follows:
![image](https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/af0b5a3a-e74b-472e-bcfb-f707c45a7eb3)

### Techniques to handle class imbalance
The dataset exhibits significant class imbalance, a common occurrence in medical imaging data, where instances of individuals without a certain condition often outnumber those with the condition. To address this issue, I employed and compared two data augmentation techniques to boost the number of instances in underrepresented classes. First, I utilized SMOTE (Synthetic Minority Over-sampling Technique), which equalized the instance counts across all classes. Second, I manually augmented the data for each class, ensuring that while each label had sufficient instances for training, the overall distribution of data remained consistent. This approach maintained the relative differences in instance counts between labels, preserving the general distribution of the dataset. The resulting distributions are illustrated below:
![image](https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/123cec7a-87b0-450a-bbe4-eaac9e43d3fb)


### So what does it mean? 
The model tends to perform better when the class distribution closely mirrors real-life scenarios. Instead of equalizing instance counts across all classes, the goal was to ensure each class had sufficient training examples while retaining the overall distribution. This approach offers a better representation of real-world conditions, enhancing the model's performance.
Model

## Model 

Some models designed on this dataset used pre-trained models like RESNET [1], VGG, and others, achieving an accuracy of close to 94%. Another model used a relatively simpler Convolutional Neural Network model to achieve a validation set accuracy of close to 80% [2]. I aim to design a simpler DNN model with fewer parameters than large models like RESNET while maintaining accuracy.

## References

[1] https://www.kaggle.com/code/mihirbhatkar/alzheimer-s-detection-using-dl

[2] https://www.kaggle.com/code/natsu18/class-prediction-pytorch

