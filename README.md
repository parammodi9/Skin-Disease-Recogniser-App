# Skin-Diseases-Detection-Web Application 🩺

![Build Status](https://github.com/parammodi9/Skin-Diseases-Detection-Web-Application/workflows/Build/badge.svg)
![Downloads](https://img.shields.io/github/downloads/parammodi9/Skin-Diseases-Detection-Web-Application/total.svg)
![Latest Release](https://img.shields.io/github/v/release/parammodi9/Skin-Diseases-Detection-Web-Application.svg)

The Skin Diseases Detection Web Application is an API designed to integrate with Android apps, providing a platform for users to detect various skin diseases without the need for physical interaction with a dermatologist.

### 🏫 University
Pandit Deendayal Energy University (PDEU)

### 👥 Team Members
- Dhairya Shah
- Sarthak Pansuria
- Param Modi
- Naman Parmar

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
7. Exported the trained model in TFLite format for deployment in the Android app.

**Android App:**
1. Used Google's example of the TFLite image_classifier model.
2. Replaced the original model files with our trained model files.
3. Added a button to redirect users to a map showing the nearest available dermatologist.
4. Modified the UI, added an app icon, and changed the name of the app.

## 🖥️ Code Files
- `image_segregation.py` - Segregates images into various categories from the HAM-10000 dataset.
- `data_aug_rem.py` - Scans the folders and performs random data removal or data augmentation to balance the number of samples per class.
- `image_classification.py` - Calls the TFLite
