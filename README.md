# From Prediction to Explanation: An Explainable Software Defect Prediction Framework for Developer Decision Support

## Overview

Software defects reduce software quality, increase maintenance costs, and may lead to system failures. While machine learning models can accurately predict software defects, most act as black-box systems, making it difficult for developers to understand the reasoning behind predictions.

This project proposes an **Explainable Software Defect Prediction Framework** that combines:

- **XGBoost** for software defect prediction
- **SHAP (SHapley Additive exPlanations)** for model interpretability
- **Google Gemini LLM** for generating developer-friendly natural language explanations

The framework predicts whether a software module is **Defective** or **Non-Defective** and explains the prediction in a way that developers can easily understand.

---

## Features

- Software defect prediction using XGBoost
- Data preprocessing and class imbalance handling
- Model evaluation using standard metrics
- SHAP-based feature importance analysis
- Natural language explanation generation using Gemini
- Developer-oriented recommendations for software quality improvement

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| Pandas | Data Processing |
| NumPy | Numerical Computing |
| Scikit-learn | Machine Learning Utilities |
| XGBoost | Defect Prediction Model |
| SHAP | Explainable AI |
| Google Gemini API | Natural Language Explanation |
| Matplotlib | Data Visualization |
| Jupyter Notebook | Model Development |

---

## Dataset

The project uses the **NASA PROMISE JM1 Software Defect Dataset**.

Dataset contains:

- Software metrics
- Defect labels (True/False)

Example metrics:

- LOC (Lines of Code)
- Cyclomatic Complexity (v(g))
- Essential Complexity (ev(g))
- Halstead Metrics
- Branch Count

---

## Project Workflow

```text
NASA PROMISE JM1 Dataset
            │
            ▼
     Data Preprocessing
            │
            ▼
     XGBoost Classifier
            │
            ▼
 Software Defect Prediction
            │
            ▼
   SHAP Explainability
            │
            ▼
 Top Contributing Features
            │
            ▼
      Gemini LLM
            │
            ▼
 Natural Language Explanation
```

---

## Project Structure

```
Software-Defect-Prediction/
│
├── dataset/
│   └── jm1.arff
│
├── notebooks/
│   ├── train.ipynb
│   ├── shap_analysis.ipynb
│   └── llm_explanation.ipynb
│
├── models/
│   └── xgboost_model.pkl
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Installation

Move into the project directory

```bash
cd software-defect-prediction
```

Create a virtual environment 

```bash
python -m venv venv
```

Activate it

Windows

```bash
venv\Scripts\activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Project

### Step 1

Load and preprocess the dataset.

### Step 2

Train the XGBoost model.

### Step 3

Generate predictions.

### Step 4

Generate SHAP explanations.

### Step 5

Use the Gemini API to convert SHAP explanations into natural language.

---

## Sample Output

### Prediction

```
Prediction: Non-Defective
```

### Important Features

```
LOC
Halstead Difficulty
Cyclomatic Complexity
Branch Count
```

### LLM Explanation

```
The software module is predicted to be non-defective because its software metrics indicate acceptable code quality and maintainability. However, the high cyclomatic complexity suggests that some functions may require refactoring to improve maintainability.
```

---

## Model Evaluation

| Metric | Value |
|---------|--------|
| Accuracy | 72.57% |
| Precision | 40.35% |
| Recall | 45.27% |
| F1-score | 42.67% |
| ROC-AUC | 67.83% |

---

## Explainability

The framework uses SHAP to:

- Identify the most influential software metrics
- Explain individual predictions
- Generate global feature importance
- Support transparent decision making

---

## Future Enhancements

- Evaluate on additional PROMISE datasets (KC1, PC1, CM1)
- Hyperparameter tuning using GridSearchCV
- Automatic software metric extraction from source code
- FastAPI deployment
- Web dashboard for prediction and explanation

---

## Author

**Nidhi**

Final Year Project

Department of Computer Science and Engineering

---

## License

This project is developed for educational and research purposes.
