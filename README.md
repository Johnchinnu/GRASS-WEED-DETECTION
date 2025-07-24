# Grass-Weed Detection Model Repository

This repository contains code and resources for detecting and classifying grass weeds using deep learning.

## File Descriptions

### 1. `train.py` - **Training the Model**
**Objective:** Train a classification model using TensorFlow and Keras, leveraging the InceptionV3 architecture with custom classification layers.

#### Key Features:
- **Data Augmentation:** Uses aggressive transformations for training and moderate ones for validation, implemented with `ImageDataGenerator`.
- **Model Architecture:** Utilizes a pretrained InceptionV3 model with added layers for task-specific classification.
- **Optimization:** Employs Adam optimizer with a custom learning rate schedule for enhanced convergence.
- **Callbacks:** Integrates EarlyStopping, ModelCheckpoint, and ReduceLROnPlateau for efficient training control.
- **Output:** Saves the trained model in `.keras` format for deployment and prediction.

---

### 2. `predict.py` - **Prediction and Visualization**
**Objective:** Predict the class of a new image and visualize activation maps to interpret the model's predictions.

#### Key Features:
- **Prediction:** 
  - Accepts an image path, preprocesses the image, and predicts its class using the saved model.
- **Grad-CAM Heatmap:** 
  - Generates heatmaps to interpret the model's focus areas, leveraging gradient-based techniques.
- **Visualization:** 
  - Creates superimposed images combining the original image with the Grad-CAM heatmap for better interpretability.

---

### 3. `app.py` - **Flask Web Application**
**Objective:** Provides a user-friendly interface for uploading images and viewing predictions and Grad-CAM heatmaps.

#### Key Features:
- **Web Interface:** 
  - Built using Flask, allowing users to upload images for classification.
- **Results Display:** 
  - Displays the predicted class and Grad-CAM heatmaps in a visually appealing format.
- **Integration:** 
  - Connects seamlessly with the trained model for backend processing.

---

### 4. `index.html` - **Frontend Template**
**Objective:** HTML template for the Flask web application.

#### Key Features:
- **Interactive Design:** 
  - Enables users to upload images and view results directly in the browser.
- **Responsive Layout:** 
  - Designed to be accessible on various devices using modern web design practices.

---

### Additional Files:
- **Dataset Folder:** Contains the training and validation images, organized into labeled subdirectories.
- **Model Checkpoints:** Saved models and logs for reproducing results.

---


### Project Screenshots

### Page to upload image
![image](https://github.com/user-attachments/assets/88a55410-df47-41bb-b6e1-b66015c7dc80)

### Image detected as **Not Weed** by the Model
![image](https://github.com/user-attachments/assets/21c5f449-e89e-477d-b2e4-f24d0751003e)

### Image detected as **Weed** by the Model
![image](https://github.com/user-attachments/assets/4b041f6e-189c-4ca7-b723-079569e7e9b3)




