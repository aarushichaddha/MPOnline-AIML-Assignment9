# 🐾 Cats vs Dogs Image Classification (CNN)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-API-red)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626)

Welcome to **Assignment 9: Image Classification using Convolutional Neural Networks (CNN)**! This repository contains a complete deep learning pipeline built from scratch to accurately classify images of cats and dogs.

## 📖 Project Overview
This project demonstrates the end-to-end process of building a Convolutional Neural Network for image classification. It explores how CNNs outperform standard Artificial Neural Networks (ANNs) for image data by preserving spatial relationships through convolution and pooling layers.

**Key Tasks Completed:**
1. **Data Understanding**: Analyzing dataset structure, class distributions, and image properties.
2. **Data Preprocessing**: Resizing images to 128x128, normalizing pixel values (0-1), and utilizing `ImageDataGenerator` for robust training/testing splits (80/20).
3. **Model Development**: Building a custom multi-layer CNN architecture from scratch using TensorFlow/Keras.
4. **Model Evaluation**: Evaluating the model using advanced metrics including Test Accuracy, Precision, Recall, F1-Score, and visualizing performance with Confusion Matrices and Epoch graphs.

## 📊 The Dataset
This project uses the famous **Cats and Dogs Classification Dataset**. 
* **Source:** [Kaggle - Dog and Cat Classification Dataset](https://www.kaggle.com/datasets/bhavikjikadara/dog-and-cat-classification-dataset)
* **Structure:** Thousands of color images separated into two distinct classes.

## 🧠 Model Architecture
The custom CNN is built with the following layers:
* **Conv2D + MaxPooling2D (32 filters):** Initial feature extraction (edges, colors).
* **Conv2D + MaxPooling2D (64 filters):** Intermediate feature extraction (textures, simple shapes).
* **Conv2D + MaxPooling2D (128 filters):** Deep feature extraction (complex object shapes).
* **Flatten:** Converts the 2D matrices into a 1D vector.
* **Dense (128 neurons):** Fully connected layer with ReLU activation.
* **Dense (1 neuron):** Output layer with Sigmoid activation for binary classification (Cat vs Dog).

## 🚀 How to Run the Project

### Option A: Run on Google Colab (Recommended)
Because image classification requires heavy computation, running this on Google Colab with a free GPU is highly recommended.
1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Change the runtime to **T4 GPU** (`Runtime > Change runtime type`).
3. Add a code cell at the top to download the dataset using the Kaggle API or `opendatasets`.
4. Click `Runtime > Run All`!

### Option B: Run Locally
If you have a powerful PC and want to run this locally:
1. Clone this repository:
   ```bash
   git clone https://github.com/aarushichaddha/MPOnline-AIML-Assignment9.git
   ```
2. Install the required dependencies:
   ```bash
   pip install tensorflow numpy matplotlib scikit-learn
   ```
3. Download the Kaggle dataset and place the extracted folder in the root directory.
4. Open `Assignment-9.ipynb` in VS Code or Jupyter Notebook and run the cells.

## 📈 Results & Evaluation
The model is evaluated not just on raw accuracy, but on holistic metrics to ensure it isn't biased toward one specific animal class. 
* **Precision & Recall**: Ensures the model isn't over-guessing a specific class.
* **F1-Score**: Provides a balanced harmonic mean of precision and recall.
* **Visualizations**: The notebook outputs detailed Matplotlib graphs charting the Loss and Accuracy across all training Epochs to monitor for overfitting.

---
*Created for AI-ML Assignment 9.*
