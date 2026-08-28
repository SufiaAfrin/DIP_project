**Course Title:** Digital Image Processing(CSE-440)
**Project Title:** - Plant Leaf Disease Classification

## Project Overview
This project implements a binary image classification model using Digital Image Processing (DIP) techniques and a Convolutional Neural Network (CNN) / Deep Learning model to classify plant leaves as **Healthy** or **Diseased**. Classify tomato leaves into two categories:
(i) Tomato Healthy
(ii)Tomato Early Blight

## Dataset Information
- **Source:**  PlantVillage Dataset - Hugging Face(https://huggingface.co/datasets/mohanty/PlantVillage)
- **Classes:** Healthy vs. Diseased Leaf Images
- **Total Images:** Insert total images, 500+ images per class
        Healthy images - 1591
        Early Blight images - 1000

## Setup & Installation
Since this project is implemented in Google Colab, no local installation is required.
1. Open the repository notebook directly in Google Colab using the **"Open in Colab"** badge inside `Plant_leaf_disease_project.ipynb`.
2. Connect to a Python 3 GPU runtime.
3. Install required dependencies if needed:
   ```bash
   pip install tensorflow opencv-python matplotlib scikit-learn
## Methodology and implementation
1. Preprocessing and Data augmentation
   Preprocessing steps:
    (i) image loading
   (ii) image resizing
   (iii) RGB image format
   (iv) Pixel normalization
   (v) Dataset splitting
3. Model Architecture: Custom CNN
   CNN Structure: Input image -> Convolutional Layer -> Activation Function -> Pooling Layer -> Convolutional Layer -> Activation Function -> Pooling Layer -> Flatten Layer -> Dense Layer -> Output Layer -> Healthy / Early Blight
4. ## Training Details & approach:
   (i)Loss Function: Binary Cross-Entropy
  (ii)Optimizer: Adam
  (iii)Epochs: [e.g., 15]
## Approach:
   The CNN model is trained using the selected PlantVillage images.

During training:
Training images are provided to the CNN in batches.
The model learns visual patterns associated with healthy and diseased leaves.
The model's prediction is compared with the actual label.
The model updates its weights to reduce classification error.
Validation data is used to monitor model performance during training.

The project uses TensorFlow/Keras for building and training the CNN model.
The trained model is saved as:
best_tomato_leaf_model.keras
## Result and Output Preview
    Training accuracy: 97%
    validation accuracy: 98%
    sample prection: 
