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
## Model Evaluation
Number of samples: 262
Actual labels: [ 87 175]
Predicted labels: [ 83 179]

Confusion Matrix:
[[ 83   4]
 [  0 175]]
Training & validation Accuracy
Epoch	Training Accuracy	Validation Accuracy	Training Loss	Validation Loss
0	1	0.9706	0.9570	0.0949	0.9377
1	2	0.9677	0.9922	0.1079	0.0386
2	3	0.9609	0.9961	0.1184	0.0111
3	4	0.9522	0.9922	0.1327	1.6440
4	5	0.9778	0.9961	0.0664	0.0198
5	6	0.9802	0.9531	0.0610	1.9803
6	7	0.9817	0.9258	0.0489	2.2490

## Result and Output Preview
    Training accuracy: 98.17%%
    validation accuracy: 92.58%
    Best Validation Accuracy: 99.61%
    sample prection:   <img width="315" height="333" alt="image" src="https://github.com/user-attachments/assets/38a36e69-d063-43bb-bdd0-b65af226f113" />

    img_h_108.jpg(image/jpeg) - 26620 bytes, last modified: 8/22/2026 - 100% done
Saving img_h_108.jpg to img_h_108.jpg
========================================
       TOMATO LEAF PREDICTION
========================================
Image: img_h_108.jpg
Predicted Class: Healthy
Confidence: 99.99 %
Raw Probability: 0.9999
 
