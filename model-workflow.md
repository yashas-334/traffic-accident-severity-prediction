# Model Workflow

## 1. Data Loading

The project uses a historical road accident dataset with details such as accident date, severity, weather, road type, light conditions, road surface condition, number of vehicles, and urban/rural area.

## 2. Feature Selection

The selected features focus on conditions that can influence accident severity:

- `Weather_Conditions`
- `Road_Type`
- `Light_Conditions`
- `Speed_limit`
- `Road_Surface_Conditions`
- `Urban_or_Rural_Area`
- `Number_of_Vehicles`
- `Junction_Detail`

## 3. Encoding

Categorical features were converted into numerical format using label encoding so they could be used by the machine learning model.

## 4. Train-Test Split

The data was split into training and testing sets using stratification to preserve the class distribution of accident severity.

## 5. Class Imbalance Handling

The dataset had an imbalanced target variable, with fewer fatal and serious accident cases compared to slight accidents. SMOTE was applied to balance the training data.

Balanced training distribution after SMOTE:

| Severity | Count |
| --- | ---: |
| Fatal | 205,227 |
| Serious | 205,227 |
| Slight | 205,227 |

## 6. Model Training

An XGBoost classifier was trained with:

- `n_estimators = 300`
- `max_depth = 6`
- `learning_rate = 0.1`
- `eval_metric = mlogloss`

## 7. Evaluation

The model was evaluated using:

- Classification report
- Confusion matrix
- Accuracy
- Precision
- Recall
- F1-score

## 8. Deployment Interface

A Streamlit interface was created to allow users to enter accident conditions and view:

- Predicted severity
- Class probabilities
- Confidence score
- Safety advisory
