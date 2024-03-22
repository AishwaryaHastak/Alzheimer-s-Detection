# Alzheimer-s-Detection

Overview -> bold text
Training a Deep Neural Network to classify images of brain MRI scans to identify Dementia and Non-Dementia Patients. 

The dataset is sourced from Kaggle and can be found at: https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images

Dealing with imbalanced classes -> make this bold text

The dataset contains images for 4 classes :
1. Mild Demented
2. Moderate Demented
3. Non Demented
4. Very Mild Demented

Distributed as follows:
![image](https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/9faaf2b4-26dc-4f99-8dc7-1c8acd21c025)


The dataset is highly imbalanced, which is usually the case in medical imaging data, where we typically tend to have higher instances of people without a certain disease and lower instances of people with a disease. I employed data augmentation techniques to increase the number of instances of the scarse classes (make this line better). First, I used SMOTE (insert full form) which balanced all classes equally, and second I manually added some augmented data to the dataset, which made the distributions look as follows:

![image](https://github.com/AishwaryaHastak/Alzheimer-s-Detection/assets/31357026/a8026e93-5a94-4d9d-9ec7-63a441e2316e)


So what does it mean?
The model performs better when the class distribution is closer to a distribution it is more likely to find in real life. So instead of all classes having equal instances, having enough training examples while also keeping the general difference in distribution was a better fit. 


Model

Some other models designed on this dataset used pre-trained models like RESNET [1], VGG, and others, to achieve an accuracy of close to 94%. Another model used a relatively simpler Convolution Neural Net model to achieve a validation set accuracy of close to 80% [2]. I aim to design a simpler DNN model with much fewer parameters than large models like RESNET and similar, while also maintaining the accuracy.




References

[1] https://www.kaggle.com/code/mihirbhatkar/alzheimer-s-detection-using-dl

[2]   
