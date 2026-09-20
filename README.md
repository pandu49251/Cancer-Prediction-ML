# Cancer Prediction (Breast Cancer - Benign or Malignant)

**Name:** _Divesh Satish Kamble_
**Course:** B.Sc. 
**Internship:** YBI Foundation - Data Science and Machine Learning

## About the Project:-

This project predicts whether a breast tumour is **benign (not cancer)** or
**malignant (cancer)** using measurements of the tumour cells. The model can be used as a
second opinion to support the pathologist.

## Dataset

- **File:** Cancer.csv (Wisconsin Breast Cancer Dataset)
- **Source:** YBI Foundation Dataset repository - https://github.com/YBIFoundation/Dataset
- **Records:** 569 samples, 33 columns
- **Target:** `diagnosis` (B = benign, M = malignant)

## Steps Followed in the Project

1. Import library
2. Import data
3. Describe data (shape, data types, missing values, target balance)
4. Data visualization (count plot, box plots, correlation chart, scatter plot)
5. Data preprocessing (remove empty and id columns, encode target, remove repeated features)
6. Define target (y) and features (X)
7. Train test split (75% training, 25% testing)
8. Modeling (Logistic Regression and Decision Tree)
9. Model evaluation (accuracy, precision, recall, confusion matrix, feature importance)
10. Prediction on a new patient
11. Explanation of the results

## Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Results

| Model | Accuracy (%) | Precision (%) | Recall (%) |
|---|---|---|---|
| **Logistic Regression** | **97.20** | **100.00** | **92.45** |
| Decision Tree | 88.81 | 93.02 | 75.47 |

Confusion matrix of Logistic Regression on the testing data:

|  | Predicted B | Predicted M |
|---|---|---|
| **Actual B** | 90 | 0 |
| **Actual M** | 4 | 49 |

Out of the 30 measurements, 10 were removed because they were highly correlated with
other features (correlation above 0.9). The model still gave 97.20% accuracy with the
remaining 20 features, and 95.80% accuracy using only the top 5 important features.

## Notebook

The complete project is in `Cancer_Prediction_Project.ipynb`. It can be opened directly
in Google Colab: **File > Upload notebook**, then **Runtime > Run all**.

## Limitations

1. The dataset has only 569 samples, which is small.
2. The model only tells benign or malignant, it cannot tell the stage of cancer.
3. This project is made for learning purpose only and must not be used for any real
   medical decision without checking by a qualified doctor.

## Future Work

- Try Random Forest, KNN and Support Vector Machine
- Balance the data using SMOTE
- Convert the model into a simple website where values can be entered to get the result
