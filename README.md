# 🚢 Titanic Survival Prediction - Data Preprocessing

This project involves preparing the Titanic dataset for survival prediction using machine learning. Below are the data preprocessing steps followed before model building.

---

## 🧹 Data Preprocessing Steps

### 🔹 1. Load the Dataset
- Import the dataset using pandas.

---

### 🔹 2. Explore the Dataset
- Inspect data types, column names, missing values, and descriptive statistics.
- Identify irrelevant or non-informative features.

---

### 🔹 3. Drop Irrelevant Columns
- Removed the following columns:
  - `PassengerId` – Just an identifier
  - `Name` – Not useful for modeling
  - `Ticket` – Random string, not predictive
  - `Cabin` – Too many missing values

---

### 🔹 4. Handle Missing Values
- Filled missing values:
  - `Age` → with **median** value
  - `Embarked` → with **mode** (most frequent port)

---

### 🔹 5. Convert Categorical Variables to Numeric
- `Sex` → Binary encoding (`male` = 0, `female` = 1)
- `Embarked` → One-hot encoding (dropping one to avoid dummy variable trap)

---

### 🔹 6. Feature Engineering
- Created new features to improve model performance:
  - `FamilySize` = `SibSp` + `Parch` + 1
  - `IsAlone` = 1 if `FamilySize` = 1, else 0

---

### 🔹 7. Feature Scaling
- Applied scaling to continuous variables:
  - Standardized `Age` and `Fare` using **StandardScaler**

---

### 🔹 8. Final Validation
- Verified that:
  - No missing values remain
  - All features are numeric and suitable for modeling

---

## ✅ Ready for Model Building

Preprocessed data is now ready to be used for classification models such as Logistic Regression, Random Forest, SVM, etc.

