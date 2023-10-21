# Skin-Disease-Recogniser-App 🩺

![Build Status](https://github.com/parammodi9/Skin-Disease-Recogniser-App/workflows/Build/badge.svg)
![Downloads](https://img.shields.io/github/downloads/parammodi9/Skin-Disease-Recogniser-App/total.svg)
![Latest Release](https://img.shields.io/github/v/release/parammodi9/Skin-Disease-Recogniser-App.svg)

The Skin Disease Recogniser is a web application designed to provide users with the ability to detect various skin diseases without the need for physical interaction with a dermatologist.

### 🏫 University
Pandit Deendayal Energy University (PDEU)

## 📝 Problem Definition
Dermatological issues are widespread worldwide and can be caused by fungal infections, bacterial infections, or allergies. The use of emerging technologies like AI and machine learning can play a significant role in diagnosing these diseases. Our solution utilizes computer vision to accurately detect the cause of skin diseases through images.

## 💡 Our Approach
**ML Model:**
1. Dataset: [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)
2. Segregated the dataset into different folders based on classes.
3. Combined and trained the TensorFlow Lite image classification model multiple times.
4. Applied two data augmentation techniques:
   - Random flipping and rotation
   - Adding random noise in addition to the above techniques
5. Tested the augmented data with two parameter inputs for the TFLite image_classifier model:
   - Dropout rate: 0.5, Epochs: 5, model_spec: efficientnet_lite0
   - Dropout rate: 0.5, Epochs: 10, model_spec: efficientnet_lite0
6. Achieved the best result with the combination of the dataset with random noise and model parameters with 10 epochs.
7. Exported the trained model in TFLite format for deployment in the web application.

**Web Application:**
1. Used the TensorFlow Lite model in our web application.
2. Added a feature to allow users to upload images for disease recognition.
3. Integrated information on various skin diseases and their possible treatments.

## 🖥️ Code Files
- `image_segregation.py` - Segregates images into various categories from the HAM-10000 dataset.
- `data_aug_rem.py` - Scans the folders and performs random data removal or data augmentation to balance the number of samples per class.
- `image_classification.py` - Calls the TFLite image_classifier model and trains it with the given dataset.

## 🛠️ Tech Stack
- TensorFlow Lite
- Python
- HTML
- CSS
- JavaScript

## 📸 Project Photos
