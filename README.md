# Traffic Accident Severity Prediction Using Machine Learning

This project predicts traffic accident severity using historical road accident data and machine learning. It focuses on identifying high-risk accident conditions and supporting better road safety decision-making.

This is a showcase repository. It explains the project workflow, dataset structure, model approach, sample outputs, and evaluation without publishing the full dataset or trained model files.

## Problem Statement

Road accidents can vary from slight to serious or fatal depending on weather, road type, lighting, speed limit, number of vehicles, surface condition, and junction details. The goal of this project is to build a machine learning model that predicts accident severity and highlights important risk factors.

## Dataset

- Dataset type: Road accident records
- Record count used in project: 307,974
- Target variable: `Accident_Severity`
- Classes: Fatal, Serious, Slight

Sample dataset preview is available in [`sample-dataset-preview.csv`](sample-dataset-preview.csv).

## Tech Stack

| Area | Tools |
| --- | --- |
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Plotly |
| Machine Learning | XGBoost, Scikit-learn |
| Class Imbalance Handling | SMOTE |
| App Interface | Streamlit |
| Model Persistence | Joblib |

## Features Used

- Weather conditions
- Road type
- Light conditions
- Speed limit
- Road surface conditions
- Urban or rural area
- Number of vehicles
- Junction detail

## Model Workflow

1. Loaded and cleaned accident records.
2. Selected key accident-related features.
3. Encoded categorical variables using label encoding.
4. Split data into training and testing sets.
5. Applied SMOTE to handle class imbalance.
6. Trained an XGBoost classifier.
7. Evaluated the model using precision, recall, F1-score, accuracy, and confusion matrix.
8. Built a Streamlit interface for severity prediction.

Detailed workflow is available in [`model-workflow.md`](model-workflow.md).

## Evaluation Summary

The model was evaluated on 60,103 test records.

| Metric | Score |
| --- | --- |
| Accuracy | 56% |
| Weighted F1-score | 64% |
| Macro F1-score | 33% |

The dataset is highly imbalanced, so SMOTE was used to improve minority-class learning for fatal and serious accidents.

## Confusion Matrix

(confusion-matrix.png)

## Streamlit App

The project includes a Streamlit interface where users can select accident conditions such as weather, road type, lighting, speed limit, and number of vehicles to predict accident severity.

### Input Form

(app-input-form.png)

### Prediction Result

(prediction-result.png)

Sample prediction output is available in [`sample-prediction-output.json`](sample-prediction-output.json).

## What I Learned

- Handling imbalanced classification problems
- Applying SMOTE for minority class balancing
- Training and evaluating an XGBoost classifier
- Building a Streamlit ML prediction interface
- Interpreting accident risk factors from structured data

## Author

Yashaswini  
GitHub: [@yashas-334](https://github.com/yashas-334)
