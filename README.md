# General Notes on Deep Learning

Deep Learning (DL) is a subset of Machine Learning (ML) that excels in handling complex data types, especially images. While numbers work well for traditional ML models, unstructured data such as images, audio files, text are where DL truly shines. Here's a breakdown:

- **Image Types in Deep Learning:**
  1. **Black and White:** 
     - Represented as binary values.
     - **0** for black and **1** for white.
  2. **Grayscale (Computer Vision):**
     - Each pixel is a number ranging from **0** (black) to **255** (white).
     - This is a pure numerical conversion where each value corresponds to a shade of gray.
  3. **Color Images (Deep Learning):**
     - Composed of three channels: **Red (R)**, **Green (G)**, and **Blue (B)**.
     - Each channel has values from **0** (darkest) to **255** (lightest) for its respective color.
     - A combination of these values creates the full color spectrum.

Deep Learning typically involves supervised learning, where the model learns from labeled data to make predictions or classifications.

Deep Learning Model Types:
* ANN - is a general-purpose neural network that can be used for a wide range of tasks, including classification, regression, and pattern recognition. 
* CNN - (Convolutional Neural Network): CNN is a type of neural network that is commonly used for image recognition and computer vision tasks.
* RNN - While CNNs are feedforward neural networks that use filters and pooling layers, whereas RNNs feed results back into the network.

# Introduction to the Face Mask Detection Project

This project focuses on building a model to detect whether individuals are wearing masks. We leverage Keras and Computer Vision algorithms, incorporating transfer learning from models like FaceNet and MobileNetV2.

## Dataset

- **Data Collection:** 
  - Two types of data collection methods are considered: manual labeling and using a folder-based dataset (where only the object of interest is present). 
  - For this project, we utilize a folder-based dataset.

## Application Flow

1. **Camera:** Captures a photo, including the background.
2. **Pretrained Model:** A pretrained model crops out only the face from the image, mimicking how the brain processes visual information.
3. **Model Input:** The cropped face image is fed into the model.
4. **Prediction:** The model predicts whether a mask is present or not.
5. **Action:** Trigger the appropriate call to action (CTA) based on the prediction.

## Model Creation and Learning Process

1. **Data Collection:** Gather images of both masked and unmasked faces.
2. **Data Preprocessing:** Crop only the face using a pretrained model called FaceNet.
3. **Data Preparation:** Convert the images into numerical and matrix formats using MobileNetV2.
4. **Model Training:** Train the model using the prepared data.
5. **Model Testing:** Evaluate the model's performance.
6. **Model Saving:** Save the best-performing model as an `.h5` file.

