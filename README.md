

# Bird Egg Multi-Class Classification with Explainable AI (Grad-CAM)

## Project Overview

This project is a deep learning-based multi-class image classification system for identifying bird egg species. It uses a convolutional neural network (CNN) trained on a labeled dataset of bird egg images and integrates Grad-CAM explainability to make model predictions interpretable.

The system also includes a full evaluation pipeline and visualization tools to analyze model performance across multiple classes.

---

## Objectives

* Build a multi-class image classification model for bird egg species
* Compare CNN architectures (ResNet18 and MobileNetV2)
* Evaluate model performance using validation and test datasets
* Improve interpretability using Grad-CAM explainability
* Visualize model behavior through performance and error analysis

---

## Key Features

### Multi-Class Classification

* Classifies 21 bird egg species
* Uses pretrained CNN models (ResNet18 / MobileNetV2)
* Trained using transfer learning for improved performance

###  Explainable AI (Grad-CAM)

* Highlights important regions in images influencing predictions
* Visualizes model “attention” during classification
* Supports analysis of correct and incorrect predictions

### Model Evaluation & Analysis

* Classification report (precision, recall, F1-score)
* Confusion matrix visualization
* Per-class accuracy analysis
* Confidence distribution (correct vs incorrect predictions)
* Model comparison (ResNet vs MobileNet)

### Advanced Diagnostics

* Misclassified sample analysis with Grad-CAM
* Class confusion ranking
* Confidence calibration curves
* Top-K prediction analysis

---

## Dataset Structure

The dataset follows a YOLO-style structure:

```
Final_Dataset/
 ├── Train/
 │    ├── images/
 │    └── labels/
 ├── Validation/
 │    ├── images/
 │    └── labels/
 └── Test/
      ├── images/
      └── labels/
```

Each label file contains a class ID corresponding to a bird species.

---

## Model Architectures

###  ResNet18

* Strong baseline CNN model
* Uses residual connections for deeper learning
* High accuracy, more computationally heavy

###  MobileNetV2

* Lightweight CNN architecture
* Optimized for efficiency
* Suitable for faster inference

---

##  Training Pipeline

* Load dataset using custom PyTorch Dataset class
* Apply image preprocessing (resize, normalize, tensor conversion)
* Train multiple models with different hyperparameters
* Validate models using validation dataset
* Select best model based on validation accuracy
* Retrain and evaluate on test dataset

---

## Evaluation Metrics

* Accuracy
* Precision / Recall / F1-score
* Confusion Matrix
* Per-class accuracy
* Confidence analysis

---

## Explainability (Grad-CAM)

Grad-CAM is used to:

* Visualize which image regions influence predictions
* Analyze misclassifications
* Improve trust in model decisions

---

## Visualizations Included

* Confusion matrix heatmap
* Model comparison bar chart
* Per-class accuracy chart
* Precision vs recall curves
* Confidence distribution plots
* Class difficulty ranking
* Misclassified image explanations (Grad-CAM)

---

## Technologies Used

* Python 
* PyTorch 
* Torchvision
* NumPy / Pandas
* Matplotlib / Seaborn
* Scikit-learn
* PIL (Image processing)
* Grad-CAM (Explainability)

---

## Key Insights

* Transfer learning significantly improved performance on small datasets
* ResNet18 generally performed better than MobileNetV2 but was heavier
* Grad-CAM helped identify model bias and misclassification patterns
* Some bird egg classes are visually similar, leading to confusion cases

---

## Future Improvements

* Improve dataset balance for similar-looking classes
* Try advanced architectures (EfficientNet, Vision Transformers)
* Add real-time Streamlit deployment interface
* Improve Grad-CAM clarity for low-confidence predictions
* Add ensemble modeling for better accuracy

---

## Project Type

Group Machine Learning Project – Multi-Class Image Classification + Explainable AI
