# Dog Vision - Dog Breed Identification

A multi-class image classification project that identifies dog breeds from photos using TensorFlow and transfer learning.

Trained on the Kaggle Dog Breed Identification dataset covering 120 breeds and ~10,000 training images. The model was also tested on custom dog photos outside the dataset, including my own dog, where the predictions came out correctly.

---

## What the project does

Given an image of a dog, the model predicts the breed out of 120 possible classes. This is a proper multi-class classification problem built using a deep learning pipeline from scratch like data loading, preprocessing, model training, evaluation, and prediction generation.

---

## Dataset

Kaggle Dog Breed Identification dataset:
- ~10,000 labeled training images
- 120 dog breeds
- Separate train and test sets
- Labels provided as a CSV mapping image IDs to breed names

---

## Approach

**Data pipeline**
- Images loaded from disk and labels converted into one-hot encoded format
- TensorFlow `tf.data` pipelines built for efficient batching, shuffling, and preprocessing
- Images resized and normalized before being fed into the model

**Transfer learning**
- Used MobileNetV2 pretrained on ImageNet as the base feature extractor
- Top layers frozen to preserve learned weights
- Custom classification head added on top for 120-class prediction
- This made training practical without needing to train from scratch on limited hardware

**Training and evaluation**
- Model trained over multiple epochs with validation tracking
- Prediction confidence checked per breed
- Best model saved for reuse and further prediction

**Kaggle submission**
- Generated prediction CSV in the format required for Kaggle evaluation
- Submitted and verified results against the leaderboard

**Custom predictions**
- Tested the trained model on real dog photos outside the dataset
- Predictions were correct, including on a personal photo of my own dog

---

## Project Structure

```bash
dog-vision-project-3/
│
├── assets/images/
├── logs/
├── models/
├── best_model.keras
├── end-to-end-dog-vision.ipynb
├── full_model_predictions_submission_1_mobilenetv2.csv
├── test_predictions.csv
├── environment-linux.yml
└── environment-windows.yml
```

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

---

## Environment

Two separate environment files are included since this project was worked on across different setups:
- `environment-windows.yml` for local Windows CPU
- `environment-linux.yml` for WSL and Google Colab

Training was done on Colab GPU. Local environments were used for experimentation and testing.

---

## Notes

Some parts follow course-guided implementation. Additional experimentation was done independently, including debugging API compatibility issues between course material and current TensorFlow versions, custom image predictions, and model improvements.
