# 🚢 Titanic Survival Prediction Using Machine Learning

## 📌 Project Overview

The **Titanic Survival Prediction** project uses Machine Learning to predict whether a passenger survived the Titanic disaster based on passenger information.

This project uses the **Random Forest Classifier** to perform binary classification. It includes data preprocessing, feature selection, model training, evaluation, and model saving using Joblib.

## 🎯 Project Objective

The main objective of this project is to build a Machine Learning classification model that predicts passenger survival based on demographic and travel-related information.

The model predicts two possible outcomes:

* **0 — Did Not Survive**
* **1 — Survived**

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Joblib
* Jupyter Notebook / Python

## 📂 Project Structure

```text
Titanic-Survival-Prediction-ML/
│
├── Data/
│   └── Titanic-Dataset.csv
│
├── Model/
│   └── model.pkl
│
├── main.py
├── requirements.txt
└── README.md
```

*Note: `main.py` represents your Python script. Adjust the filename if your script has a different name.*

## 📊 Dataset Information

The project uses the Titanic dataset stored in `Data/Titanic-Dataset.csv`.

### Features Used

| Feature  | Description                          |
| -------- | ------------------------------------ |
| Pclass   | Passenger ticket class               |
| Sex      | Passenger's sex                      |
| Age      | Passenger's age                      |
| SibSp    | Number of siblings or spouses aboard |
| Parch    | Number of parents or children aboard |
| Fare     | Passenger fare                       |
| Embarked | Port of embarkation                  |

### Target Variable

**Survived**

* `0`: Passenger did not survive.
* `1`: Passenger survived.

## ⚙️ Project Workflow

### 1. Data Loading

Loaded the Titanic dataset using Pandas.

### 2. Feature Selection

Selected seven input features: Pclass, Sex, Age, SibSp, Parch, Fare, and Embarked.

### 3. Data Preprocessing

Handled missing values using SimpleImputer.

* Numerical features: Missing values filled using the median.
* Categorical features: Missing values filled using the most frequent value.

### 4. Feature Scaling

Applied StandardScaler to numerical features.

### 5. Categorical Encoding

Applied OneHotEncoder to convert categorical features into numerical representations.

### 6. Pipeline Creation

Used ColumnTransformer and Pipeline to combine preprocessing and model training into a single workflow.

### 7. Model Training

Trained a Random Forest Classifier with 100 decision trees.

### 8. Model Evaluation

Evaluated the model using a train-test split and accuracy score. The code also imports classification-report and confusion-matrix metrics for further evaluation.

### 9. Model Saving

Saved the trained machine learning pipeline as `model.pkl` using Joblib.

## 🤖 Machine Learning Algorithm

### Random Forest Classifier

Random Forest is a supervised machine learning algorithm that combines multiple decision trees to make predictions.

In this project, it classifies passengers into two categories:

* Survived
* Did not survive

The model is configured with 100 estimators and a random state of 42.

## 📈 Model Evaluation

The dataset is divided into training and testing sets:

* Training data: 80%
* Testing data: 20%

The model is evaluated using accuracy.

**Actual model accuracy:** Run the Python script to obtain the accuracy for your dataset. Do not assume a result without running the model.

## 💾 Model Deployment Preparation

The trained model is saved in the following location:

`Model/model.pkl`

The saved pipeline includes preprocessing and classification steps, allowing the same transformations to be applied when making predictions on new passenger data.

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone <your-github-repository-url>
```

### Step 2: Navigate to the Project Folder

```bash
cd Titanic-Survival-Prediction-ML
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Check the Dataset

Make sure the dataset is available at:

`Data/Titanic-Dataset.csv`

### Step 5: Run the Python Script

```bash
python main.py
```

After execution, the script displays the model's accuracy and saves the trained model as `Model/model.pkl`.

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
pandas
numpy
scikit-learn
joblib
```

## 🔮 Future Improvements

* Build an interactive web application using Streamlit.
* Add a confusion matrix and classification report.
* Evaluate the model using precision, recall, and F1-score.
* Perform hyperparameter tuning to improve model performance.
* Deploy the application online for real-time predictions.

## 👨‍💻 Author

**Rohit Tayde**

Machine Learning Project

## 📝 Conclusion

This project demonstrates the implementation of a complete machine learning classification workflow, including data preprocessing, feature engineering, model training, evaluation, and model serialization. It provides a foundation for building and deploying predictive machine learning applications.
