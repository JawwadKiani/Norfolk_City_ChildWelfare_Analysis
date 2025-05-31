# Norfolk_City_ChildWelfare_Analysis

This project performs predictive modeling on Norfolk City's child welfare data to analyze adoption outcomes. The goal is to build classification models that can predict whether a child will be adopted based on demographic features such as age, gender, and race.

## 📁 Dataset

The dataset used (`adoption.csv`) contains aggregated counts of children in different demographic groups along with adoption outcomes. Key features include:

- **Demographics**: `Male`, `Female`, `Black`, `White`, `Hispanic`
- **Age Groups**: `Age.Under.1`, `Age.1.Through.5`, `Age.6.Through.9`
- **Target Variable**: `Adopted` (derived from `Left.Through.Adoption`)

## 🧠 Models Used

- Logistic Regression
- Random Forest
- Decision Tree (with tuning)
- K-Nearest Neighbors (KNN)
- XGBoost

All models were trained using **caret** with 5-fold cross-validation repeated 3 times. The target variable was preprocessed as a binary factor (`Yes` for adopted, `No` otherwise), and features were scaled as needed.

## 📊 Evaluation Metrics

Each model was evaluated using:

- Area Under the ROC Curve (AUC)
- Accuracy
- Sensitivity (Recall for the Positive Class)
- Specificity (Recall for the Negative Class)

AUC and accuracy scores were plotted to compare model performance.

## 🌳 Final Model

The **Tuned Decision Tree** model was selected for interpretation and visualization:

- **AUC**: 0.73
- **Accuracy**: 68%
- **Sensitivity**: 66.7%
- **Specificity**: 69.6%
- **Kappa**: 0.36

A visual of the final tree was generated using `rpart.plot`.

## 🔧 Technologies & Packages

- `caret` – Model training and cross-validation
- `randomForest`, `rpart`, `kknn`, `xgboost` – ML algorithms
- `pROC`, `e1071` – Evaluation
- `ggplot2`, `rpart.plot` – Visualization
- `doParallel` – Parallel processing

## 🚀 How to Reproduce

1. Clone the repository.
2. Place the `adoption.csv` file in the project root.
3. Open the R Markdown file in RStudio.
4. Run the entire script or render to HTML.

## 📌 Author

**Muhammad Jawwad Kiani**  
Senior Data Analyst | Norfolk City Analysis Project  
📅 Date: May 31, 2025
