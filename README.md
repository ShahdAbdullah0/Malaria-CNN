# 🦠 Malaria Cell Image Classification using CNN

## 📌 Project Overview

This project uses a **Convolutional Neural Network (CNN)** to classify microscopic blood cell images into two categories:

* **Parasitized**
* **Uninfected**

The goal is to build a deep learning image classification model capable of distinguishing between infected and uninfected cells.

## 🎯 Objective

The main objective of this project is to apply a complete deep learning workflow for image classification, including:

* Loading and exploring the dataset
* Image preprocessing
* Data normalization
* Building a CNN model
* Training the model
* Evaluating the model's performance

## 📊 Dataset

The dataset contains microscopic cell images divided into two classes:

| Class       | Description                        |
| ----------- | ---------------------------------- |
| Parasitized | Cells containing malaria parasites |
| Uninfected  | Healthy/uninfected cells           |

The dataset contains **27,558 images**, with **13,779 images per class**.

## 🔧 Data Preprocessing

The images were prepared before training using several preprocessing steps:

* Resizing images to **128 × 128 pixels**
* Converting images into numerical arrays
* Normalizing pixel values to the range **0–1**
* Preparing the data for input into the CNN model

## 🧠 Convolutional Neural Network

A CNN was used because convolutional neural networks are particularly effective for image classification and can automatically learn visual features from images.

The model learns hierarchical image features during training, starting with simple patterns and progressing toward more complex features useful for distinguishing the two classes.

## 📈 Model Training & Evaluation

The model was trained on the prepared malaria cell images and evaluated using classification performance metrics.

The notebook includes the complete workflow for training and evaluating the model.

> The detailed implementation, experiments, and results are available in the Jupyter Notebook included in this repository.

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook / Google Colab
* Convolutional Neural Networks (CNN)

## 📂 Project Structure

```text
Malaria-CNN/
│
├── Malaria_CNN_LinkedIn.ipynb
└── README.md
```

## ▶️ How to Run

The notebook was developed using **Google Colab**.

To run the project:

1. Open the notebook.
2. Upload or connect the required dataset.
3. Install/import the required libraries.
4. Run the notebook cells sequentially.

## 💡 What I Learned

Through this project, I practiced:

* Image data preprocessing
* Working with large image datasets
* CNN architecture and image classification
* Data normalization
* Model training and evaluation
* Using TensorFlow/Keras for deep learning projects

## 👩‍💻 Author

**Shahd Abdullah**
**Samaa Mohamed**
**Shahd Reda**

Computer Science & Artificial Intelligence Student
Benha University

GitHub: [ShahdAbdullah0](https://github.com/ShahdAbdullah0)
