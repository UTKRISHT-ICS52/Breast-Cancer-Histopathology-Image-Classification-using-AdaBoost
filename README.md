
# Breast Cancer Histopathology Image Classification using AdaBoost

## Project Overview

This project implements the AdaBoost (Adaptive Boosting) ensemble learning algorithm for breast cancer histopathology image classification using the IDC dataset.

The objective is to classify histopathology image patches into two categories:
- Non-Cancerous (Class 0)
- Cancerous (Class 1)

Histogram of Oriented Gradients (HOG) is used for feature extraction, followed by AdaBoost model training, hyperparameter tuning, and performance evaluation.

## Dataset

**Dataset:** IDC Regular Histopathology Image Dataset

- Total images: Approximately 277,524
- Total patients: 279
- Image format: PNG
- Image type: RGB histopathology patches
- Original image dimensions: 50 × 50 pixels

Dataset source: Kaggle - Breast Histopathology Images

## Technologies Used

- Python
- NumPy
- Pandas
- OpenCV
- Scikit-image
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib

## Methodology

1. Import required libraries.
2. Load the IDC histopathology dataset.
3. Display sample images.
4. Perform patient-wise train, validation, and test splitting.
5. Create balanced datasets.
6. Extract HOG features.
7. Implement the AdaBoost classifier.
8. Perform hyperparameter tuning.
9. Select the best model using validation F1-score.
10. Evaluate the final model on the test dataset.
11. Generate confusion matrix and ROC curve.
12. Analyze feature importance.
13. Save the trained model and experimental results.

## Feature Extraction

HOG (Histogram of Oriented Gradients) is used to extract image gradient and texture-related features.

Configuration:

- Image size: 64 × 64
- Orientations: 9
- Pixels per cell: 8 × 8
- Cells per block: 2 × 2
- HOG features per image: 1,764

## Dataset Splitting

Patient-wise splitting is performed using GroupShuffleSplit to reduce patient-level data leakage.

- Training pool: 80%
- Testing: 20%
- Validation: 15% of the training pool

Balanced experimental subsets:

- Training: 4,000 images
- Validation: 2,000 images
- Testing: 2,000 images

## AdaBoost Hyperparameter Tuning

The following configurations were evaluated:

| Parameter | Values |
|---|---|
| n_estimators | 50, 100, 150, 200 |
| learning_rate | 0.01, 0.1, 0.5, 1.0 |

The best configuration was selected based on validation F1-score.

## Model Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix
- ROC Curve

## Results

Add your actual experimental results below:

| Metric | Test Score |
|---|---|
| Accuracy | Add your result |
| Precision | Add your result |
| Recall | Add your result |
| F1-Score | Add your result |
| ROC-AUC | Add your result |

**Best Hyperparameters:**
- Number of Estimators: Add your value
- Learning Rate: Add your value

## Project Files

- `best_adaboost_model.pkl` – Trained AdaBoost model
- `adaboost_hyperparameter_results.csv` – Hyperparameter tuning results
- `adaboost_feature_importance.csv` – Feature importance values
- `adaboost_final_results.csv` – Final evaluation metrics

## Installation

Clone the repository:

```bash
git clone https://github.com/https://github.com/UTKRISHT-ICS52/breast-cancer-histopathology-adaboost.git
```

Install dependencies:

```bash
pip install numpy pandas opencv-python scikit-image scikit-learn matplotlib seaborn joblib
```

## Future Scope

- Compare AdaBoost with Random Forest, Decision Tree, KNN, and CNN.
- Explore advanced feature extraction methods.
- Investigate ensemble learning improvements.
- Evaluate model generalization on independent datasets.

## Disclaimer

This project is intended for academic research and educational purposes only. It is not a clinically validated diagnostic system and should not be used for medical decision-making.

## Author

**Utkrisht Patel**

Researcher | Machine Learning | AI | Hardware & IoT

---

If you find this project useful, consider giving the repository a star!
