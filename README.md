
# Earthquake Damage Prediction

The 2015 Gorkha earthquake caused widespread devastation across Nepal. This project uses building survey data to predict whether a building suffered low, medium, or high damage, helping support building risk assessment and disaster preparedness.

The tuned Decision Tree model achieved an **accuracy of 70.46%**, a **Macro F1 Score of approximately 0.64**, and **60% recall for Grade 3 severe damage**.

## Dataset

- **Source:**  DrivenData — Richter's Predictor: Modeling Earthquake Damage
- **Size:** 260,601 buildings
- **Target:** `damage_grade` — 1 (Low), 2 (Medium), 3 (Severe)

## Project Structure

```text
Earthquake-Damage-Prediction/
├── Modeling_earthquake_damage(6).ipynb
├── README.md
└── .gitignore
```

## Setup & Usage

### Requirements

```text
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

Install with:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### How to Run

1. Download the dataset from the link above.
2. Extract the dataset files.
3. Place `train_values.csv` and `train_labels.csv` where the notebook expects them.
4. Open `Modeling_earthquake_damage(6).ipynb`.
5. Run all cells from top to bottom.

## Methodology

### Preprocessing

- Checked missing values and duplicate records.
- Prepared numerical and categorical features.
- Encoded categorical variables where required.
- Separated input features and the target variable.

### Model

- **Algorithm:** Tuned Decision Tree Classifier
- **Initial Model Comparison:** Five classification models
- **Model Selection:** Decision Tree performed best among the initial models
- **Evaluation Metrics:** Accuracy, Macro F1 Score, and Grade 3 Recall

## Key Findings

| **Finding** | **Detail** |
|---|---|
| **Geographic features** | Geographic ID features were important predictors of building damage grades. |
| **Foundation type** | Foundation type was also identified as an important predictor. |
| **Severe damage detection** | Grade 3 recall was 60%. |
| **Model selection** | The tuned Decision Tree was selected after comparing five initial classification models. |

## Results

| **Metric** | **Score** |
|---|---:|
| Accuracy | **70.46%** |
| Macro F1 Score | **~0.64** |
| Grade 3 Recall | **60%** |

## Limitations

- The model does not correctly identify every severely damaged building.
- Geographic patterns in the training data may not generalize to other earthquake-prone regions.
- Independent-data validation is needed before applying the model to new regions.
- Predictions should not replace professional structural inspections.

## Data Source & Acknowledgement

## **Data Source & Acknowledgement**

The dataset is from [DrivenData — Richter's Predictor: Modeling Earthquake Damage](https://www.drivendata.org/competitions/57/nepal-earthquake/) and was used as part of the DataMites PRCP-1015 Capstone Project.

Please refer to the competition page for the dataset details and applicable terms of use before redistributing the data.
