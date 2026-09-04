# 🐱 Cat vs Dog Image Classification Using CNN

A Convolutional Neural Network (CNN) project that classifies images as either **cats or dogs** using TensorFlow and Keras.

## 📌 Project Overview

This project demonstrates how a CNN can be used for binary image classification.

The model learns visual features from cat and dog images and predicts the class of a new image. **Data augmentation** is also used to improve generalization and reduce overfitting.

## 📂 Dataset

The dataset contains two classes:

- 🐱 Cats
- 🐶 Dogs

| Dataset | Number of Images |
|---|---:|
| Training | 8,005 |
| Testing | 2,023 |

All images are resized to **128 × 128 pixels** before being given to the CNN.

*Dataset Source:* [Kaggle Cat and Dog Dataset](https://www.kaggle.com/datasets/tongpython/cat-and-dog)

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 🔄 Data Augmentation

The following augmentation techniques were applied to training images:

- Random horizontal flipping
- Random rotation
- Random zoom

Data augmentation creates slightly different versions of training images, helping the model learn more general features.

## 🧠 CNN Architecture

The model consists of:

1. Input layer — `128 × 128 × 3`
2. Data augmentation
3. Pixel normalization
4. Convolutional layer — 32 filters
5. Max Pooling
6. Convolutional layer — 64 filters
7. Max Pooling
8. Convolutional layer — 128 filters
9. Max Pooling
10. Flatten layer
11. Dense layer — 128 neurons
12. Dropout — 50%
13. Sigmoid output layer

The final sigmoid layer is used because this is a **binary classification** problem.

## ⚙️ Model Compilation

The model uses:

- **Optimizer:** Adam
- **Loss function:** Binary Cross-Entropy
- **Metric:** Accuracy

## 📊 Model Performance

The trained model achieved:

| Metric | Result |
|---|---:|
| Test Accuracy | **80.47%** |
| Test Loss | **0.4282** |

The model was also evaluated using a confusion matrix and classification report.

### Classification Report

| Class | Precision | Recall | F1-Score |
|---|---:|---:|---:|
| Cats | 0.80 | 0.81 | 0.81 |
| Dogs | 0.81 | 0.80 | 0.80 |

## 🔍 Testing on New Images

The trained model was tested on individual unseen cat and dog images.

The model successfully classified the sample cat and dog images correctly.

Prediction Examples: <br>
| Sample Image | Model Prediction |
| :---: | :---: |
| <img width="85" height="55" alt="dog1" src="https://github.com/user-attachments/assets/b3f018e6-4019-4a3b-9b0c-8287b0fc44f8" /> | **Dog** |
| <img width="55" height="85" alt="cat1" src="https://github.com/user-attachments/assets/66a963ef-e23a-4d84-939b-9e9e922283e2" /> | **Cat** |




## 📁 Project Structure

```text
cat-dog-cnn/
│
├── cat_dog_cnn.ipynb
└── README.md
```


## 💻 How to Run

1. **Clone the repository:** <br>
   git clone https://github.com/Sandhya-Bhusal/cat_dog_cnn.git

2. **Install required packages:** <br>
   ```pip install tensorflow numpy matplotlib seaborn scikit-learn```

3. **Run the model:** <br>
   Open [cat_dog_cnn.ipynb](Cat_Dog_CNN.ipynb) in Jupyter Notebook or Google Colab.
