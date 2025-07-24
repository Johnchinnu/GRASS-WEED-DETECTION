# GRASS-WEED-DETECTION
# 🌿 Grass Weed Detection using Deep Learning

This project is a Flask-based web application for detecting grass weeds in images using a convolutional neural network model based on InceptionV3. The app supports image uploads, performs classification, and visualizes results using Grad-CAM heatmaps and overlays.

---

## 📁 Files Overview

### 🔹 `train.py`
- Trains an image classification model using TensorFlow and Keras.
- Uses the InceptionV3 architecture (without the top layer).
- Applies aggressive data augmentation for training and moderate augmentation for validation.
- Saves the model to `trained_model.keras`.

### 🔹 `predict.py`
- Loads the trained model (`trained_model.keras`).
- Provides:
  - `predict_image()` to classify a single image.
  - `generate_heatmap()` to produce Grad-CAM heatmaps and overlay images.

### 🔹 `app.py`
- Flask application backend:
  - Handles image upload and validation.
  - Calls prediction and heatmap functions from `predict.py`.
  - Saves images and renders results to `index.html`.

### 🔹 `index.html`
- HTML template for the web interface.
- Allows users to upload images.
- Displays:
  - Original image
  - Predicted class label
  - Grad-CAM heatmap
  - Overlay image

---

## 🚀 How to Run

### 1. Install Required Libraries

```bash
pip install flask tensorflow opencv-python numpy matplotlib
