# Melanoma Detection using CNN
## Problem Statement
In this assignment, you will build a **multiclass classification model using a custom convolutional neural network in tensorflow.**

**Problem statement:** To build a CNN based model which can accurately detect **melanoma**. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

You can download the dataset [here]([url](https://airlock-on-edge.woolf.university/?url=https%3A%2F%2Fdrive.google.com%2Ffile%2Fd%2F1xLfSQUGDl8ezNNbUkpuHOYvSpTyxVhCs%2Fview%3Fusp%3Dsharing&resourceId=5694242&studentId=3ff828dc-d0aa-4a29-b3cd-8d64e1c2f77f&token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjNmZjgyOGRjLWQwYWEtNGEyOS1iM2NkLThkNjRlMWMyZjc3ZiIsImlzVmVyaWZpZWQiOnRydWUsImtpbmQiOiJvYXV0aCIsIm9yZyI6eyJncm91cHMiOltdLCJpZCI6Ijk3ZjhjNTRmLWVjZjctNGY1YS1iNGQ3LWM4NWEwMDI2ZGEwNyJ9LCJzY29wZSI6IioiLCJpYXQiOjE3NTcwODU4MTcsImV4cCI6MTc1NzY5MDYxNywiaXNzIjoidXJuOldvb2xmVW5pdmVyc2l0eTpzZXJ2ZXIvdXNlci9hY2Nlc3MifQ.xdrJJjgfLvGH02m0dDGDfM3c9T92nF24s5kwKdQztLE)).

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the **International Skin Imaging Collaboration (ISIC)**. All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
The data set contains the following diseases:
- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion 

## Project Pipeline
- **Data Reading/Data Understanding** → Defining the path for train and test images 
- **Dataset Creation** → Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
- **Dataset visualisation** → Create a code to visualize one instance of all the nine classes present in the dataset
- **Model Building & training**:
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~20 epochs
  - Write your findings after the model fit, see if there is evidence of model overfit or underfit
- **Choose an appropriate data augmentation strategy to resolve underfitting/overfitting**
- **Model Building & training on the augmented data**:
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~20 epochs
  - Write your findings after the model fit, see if the earlier issue is resolved or not?
- **Class distribution**: Examine the current class distribution in the training dataset 
  - Which class has the least number of samples?
  - Which classes dominate the data in terms of the proportionate number of samples?
- **Handling class imbalances**: Rectify class imbalances present in the training dataset with [Augmentor]([url](https://airlock-on-edge.woolf.university/?url=https%3A%2F%2Faugmentor.readthedocs.io%2Fen%2Fmaster%2F&resourceId=5694242&studentId=3ff828dc-d0aa-4a29-b3cd-8d64e1c2f77f&token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjNmZjgyOGRjLWQwYWEtNGEyOS1iM2NkLThkNjRlMWMyZjc3ZiIsImlzVmVyaWZpZWQiOnRydWUsImtpbmQiOiJvYXV0aCIsIm9yZyI6eyJncm91cHMiOltdLCJpZCI6Ijk3ZjhjNTRmLWVjZjctNGY1YS1iNGQ3LWM4NWEwMDI2ZGEwNyJ9LCJzY29wZSI6IioiLCJpYXQiOjE3NTcwODU4MTcsImV4cCI6MTc1NzY5MDYxNywiaXNzIjoidXJuOldvb2xmVW5pdmVyc2l0eTpzZXJ2ZXIvdXNlci9hY2Nlc3MifQ.xdrJJjgfLvGH02m0dDGDfM3c9T92nF24s5kwKdQztLE)) library.
- **Model Building & training on the rectified class imbalance data**:
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~30 epochs
  - Write your findings after the model fit, see if the issues are resolved or not?
