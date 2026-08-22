# 🦠 Malaria Cell Image Classification using CNN

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** for classifying microscopic blood cell images into two classes:

* **Parasitized**
* **Uninfected**

The project covers the complete deep learning workflow, including image preprocessing, data augmentation, model building, training, and evaluation.

## 🎯 Objective

The main objective is to develop a CNN-based image classification model capable of distinguishing between malaria-infected and uninfected blood cell images.

## 📊 Dataset

The dataset contains **27,560 images** distributed equally between the two classes:

| Class       | Number of Images |
| ----------- | ---------------: |
| Parasitized |           13,780 |
| Uninfected  |           13,780 |

For model training and validation, an **80/20 validation split** was used:

* **Training:** 22,048 images
* **Validation:** 5,510 images

## 🔧 Image Preprocessing

The images were processed before being used by the model.

### Preprocessing steps

* Converted images to **RGB**
* Resized images to **128 × 128**
* Converted images into NumPy arrays
* Normalized pixel values to the range **0–1**

### Data Augmentation

`ImageDataGenerator` was used to improve model generalization through:

* Rotation
* Width shifting
* Height shifting
* Zooming
* Horizontal flipping

The images were also rescaled using `1./255`.

## 🧠 CNN Architecture

The model was built using **TensorFlow/Keras**.

The architecture consists of three convolutional blocks:

* `Conv2D(32)` + Batch Normalization + Max Pooling + Dropout
* `Conv2D(64)` + Batch Normalization + Max Pooling + Dropout
* `Conv2D(128)` + Batch Normalization + Max Pooling + Dropout

This is followed by:

* Flatten layer
* Dense layer with **128 neurons**
* Dropout
* Final Dense layer with **1 neuron and sigmoid activation**

The model contains approximately **3.3 million trainable parameters**.

## ⚙️ Training Configuration

The model was compiled using:

* **Optimizer:** Adam
* **Loss Function:** Binary Crossentropy
* **Metric:** Accuracy

Two callbacks were used during training:

* **EarlyStopping** to stop training when validation loss stopped improving
* **ReduceLROnPlateau** to reduce the learning rate when validation performance plateaued

Although the maximum number of epochs was set to 50, training stopped after **8 epochs** due to the training callbacks.

## 📈 Results

The final recorded training results were:

* **Training Accuracy:** 94.67%
* **Validation Accuracy:** 94.08%
* **Validation Loss:** 0.1722

The classification report on the **5,510 validation images** showed:

| Class                | Precision | Recall | F1-Score |
| -------------------- | --------: | -----: | -------: |
| Parasitized          |      0.96 |   0.92 |     0.94 |
| Uninfected           |      0.92 |   0.96 |     0.94 |
| **Overall Accuracy** |           |        | **0.94** |

These results show that the model achieved approximately **94% validation accuracy** while maintaining balanced performance between the two classes.

## 🛠️ Technologies Used

* **Python**
* **TensorFlow / Keras**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Pillow**
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

To run the notebook:

1. Open `Malaria_CNN.ipynb`.
2. Prepare the malaria cell image dataset.
3. Make sure the dataset follows the required folder structure.
4. Install/import the required libraries.
5. Run the notebook cells sequentially.

Expected dataset structure:

```text
cell_images/
└── Parasitized/
└── Uninfected/
```

## 💡 Key Learning Outcomes

Through this project, I practiced:

* Working with image datasets
* Image preprocessing and normalization
* Data augmentation
* Building CNN architectures
* Using Batch Normalization and Dropout
* Training deep learning models with TensorFlow/Keras
* Applying Early Stopping and learning-rate scheduling
* Evaluating classification models using precision, recall, F1-score, and accuracy

## 👩‍💻 Author

* **Shahd Abdullah**
* **Samaa Mohamed**
* **Shahd Reda**

Computer Science and Artificial Intelligence Student
Benha University

GitHub: [ShahdAbdullah0](https://github.com/ShahdAbdullah0)
