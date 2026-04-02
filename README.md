# PRML_Project-Face_Recognition

*A study of facial recognition techniques and classifier / feature-extraction combinations*

## 🚀 Project Overview

This project attempts to explore and evaluate different methods for facial recognition — specifically to find the best combination of:
- feature extraction techniques (e.g., eigenfaces, LBP, raw pixels)
- feature reduction / dimensionality reduction methods (e.g., PCA, LDA)
- classifiers (e.g., SVM, k-NN, Logistic Regression)

The goal is to train a model with the highest possible accuracy for face recognition.

This project is part of a course on Pattern Recognition & Machine Learning (PRML).

## 📁 Repository Structure
```
├── feature_extraction/     # Code for various feature extraction techniques
├── helper/                 # Utility/helper scripts (data loading, preprocessing)
├── models/                 # Classifier implementations / trained models
├── eda.ipynb              # Exploratory Data Analysis notebook
├── README.md              # This file
└── LICENSE                # MIT License
```

## 🧠 Methods & Techniques

### Feature extraction
- Raw pixel values
- Eigenfaces (Principal Component Analysis on faces)
- Local Binary Patterns (LBP)
- … (feel free to list any others your code supports)

### Dimensionality reduction
- Principal Component Analysis (PCA)
- Linear Discriminant Analysis (LDA)
- …

### Classifiers
- Support Vector Machine (SVM)
- k-Nearest Neighbors (k-NN)
- Logistic Regression
- …

## 📊 Experiments & Evaluation

In the EDA notebook (`eda.ipynb`), you will find:
- Dataset overview (number of subjects, images per subject)
- Example face images
- Preprocessing steps (cropping, resizing, grayscale, normalization)
- Comparison of feature-extraction + classifier pipelines
- Performance metrics: accuracy, confusion matrix, possibly ROC/PR curves

## 📥 Getting Started

### Prerequisites
- Python 3.x
- Required libraries: `numpy`, `scikit-learn`, `matplotlib`, `opencv-python` (or `Pillow`), `pandas`, etc.
```bash
pip install -r requirements.txt
```

> **Note:** If `requirements.txt` is not included yet, create one with required dependencies.

### Data Setup
1. Acquire the face-recognition dataset used for experiments. (For example: the ORL, Yale, or your custom dataset.)
2. Place images in a folder structure like:
```
data/
  subject1/
    image1.jpg
    image2.jpg
    …
  subject2/
    …
```
3. In `helper/` code, ensure the data loader points to the correct dataset folder path.

### Running the Experiments

To run feature extraction and training:
```bash
python helper/data_loader.py              # loads & preprocesses data
python feature_extraction/extract_features.py   # extracts features
python models/train_classifier.py         # trains model
```

To evaluate new images (face recognition/prediction):
```bash
python models/predict_face.py --image path/to/image.jpg
```

> Adjust the file names based on your actual code.


## 🔧 Customisation & Extension

You can extend or modify this project by:
- Trying additional feature extraction methods (e.g., Gabor filters, deep-learning embeddings)
- Using more advanced classifiers (e.g., Random Forest, XGBoost, Neural Networks)
- Experimenting with image augmentation (rotation, scaling, illumination changes)
- Deploying a real-time face recognition application (e.g., webcam feed)
- Comparing with deep-learning-based face embeddings (e.g., FaceNet, ArcFace)

