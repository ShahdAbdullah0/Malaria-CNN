# 🦠 Malaria Cell Image Classification using CNN

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** for classifying microscopic blood cell images into two classes:

* **Parasitized**
* **Uninfected**

The project covers a complete deep learning workflow, including data exploration, image preprocessing, data augmentation, CNN model development, training, and evaluation.

## 🎯 Objective

The main objective of this project is to develop a deep learning model capable of distinguishing between malaria-infected and uninfected blood cell images.

## 📊 Dataset

The dataset contains **27,560 microscopic cell images**, distributed equally between the two classes:

| Class       | Number of Images |
| ----------- | ---------------: |
| Parasitized |           13,780 |
| Uninfected  |           13,780 |

An **80/20 validation split** was used for model training:

* **Training:** 22,048 images
* **Validation:** 5,510 images

## 🔧 Image Preprocessing

The images were prepared before being passed to the CNN model.

### Preprocessing steps

* Images were converted to **RGB**
* Images were resized to **128 × 128 pixels**
* Pixel values were normalized to the range **0–1**
* Images were prepared using `ImageDataGenerator`

### Data Augmentation

Data augmentation was applied to improve model generalization using:

* Rotation
* Width shifting
* Height shifting
* Zooming
* Horizontal flipping

## 🧠 CNN Architecture

The model was implemented using **TensorFlow/Keras**.

The architecture contains three convolutional blocks with increasing numbers of filters:

* **32 filters**
* **64 filters**
* **128 filters**

The convolutional layers are combined with:

* Batch Normalization
* Max Pooling
* Dropout

The convolutional feature extractor is followed by:

* Flatten layer
* Dense layer with **128 neurons**
* Dropout
* Final Dense layer with **1 neuron**
* Sigmoid activation for binary classification

The model contains approximately **3.3 million trainable parameters**.

## ⚙️ Training Configuration

The model was compiled using:

* **Optimizer:** Adam
* **Loss Function:** Binary Crossentropy
* **Metric:** Accuracy

Two callbacks were used:

* **EarlyStopping** with `patience=3` and `restore_best_weights=True`
* **ReduceLROnPlateau** for adaptive learning-rate reduction

The maximum number of epochs was set to **50**. The EarlyStopping callback automatically stopped training when validation loss stopped improving.

In the latest training run, the model reached **Epoch 16/50** before training stopped.

## 📈 Results

During training, the best recorded validation accuracy was:

**94.23% at Epoch 12**

At Epoch 12:

* Training Accuracy: **95.09%**
* Validation Accuracy: **94.23%**
* Validation Loss: **0.1797**

The final evaluation on the validation set produced:

* **Validation Loss:** 0.1746
* **Validation Accuracy:** **93.94%**

### Classification Report

| Class                | Precision | Recall | F1-Score |   Support |
| -------------------- | --------: | -----: | -------: | --------: |
| Parasitized          |      0.96 |   0.93 |     0.94 |     2,755 |
| Uninfected           |      0.93 |   0.96 |     0.94 |     2,755 |
| **Overall Accuracy** |           |        | **0.94** | **5,510** |

The classification report shows balanced performance between the two classes, with an overall accuracy of approximately **94%** on the validation set.

## 🛠️ Technologies Used

* **Python**
* **TensorFlow / Keras**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Pillow**
* **Scikit-learn**
* **Google Colab**
* **Convolutional Neural Networks (CNN)**

## 📂 Project Structure

```text
Malaria-CNN/
│
├── Malaria_CNN.ipynb
├── README.md
└── requirements.txt
```

## ▶️ How to Run

The project was developed using **Google Colab**.

To run the project:

1. Open `Malaria_CNN.ipynb`.
2. Prepare the malaria cell image dataset.
3. Make sure the dataset contains the required class folders.
4. Install or import the required libraries.
5. Run the notebook cells sequentially.

Expected dataset structure:

```text
cell_images/
├── Parasitized/
└── Uninfected/
```

## 💡 Key Learning Outcomes

Through this project, we practiced:

* Working with image datasets
* Image preprocessing and normalization
* Data augmentation
* Building CNN architectures
* Batch Normalization and Dropout
* Training deep learning models using TensorFlow/Keras
* Using EarlyStopping and learning-rate scheduling
* Evaluating classification models
* Using precision, recall, F1-score, and accuracy for model evaluation

## 👥 Team

This project was developed collaboratively by:

* **Shahd Abdullah Mohamed Reda**
* **Samaa Mohamed Ali**
* **Shahd Reda El-Gohary**

## 👩‍💻 Authors

* **Shahd Abdullah Mohamed Reda**
* **Samaa Mohamed Ali**
* **Shahd Reda El-Gohary**


Computer Science and Artificial Intelligence Student — Benha University
---

### 📌 Project Repository

The complete implementation is available in this repository, including the Jupyter Notebook and project documentation.
