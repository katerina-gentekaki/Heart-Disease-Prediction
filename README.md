# ❤️ Heart Disease Prediction using Machine Learning

This project uses machine learning models to predict the presence of heart disease based on patient data. It compares two classification algorithms — Logistic Regression and Decision Tree — and selects the better-performing model based on accuracy and F1 score.

---

## 📁 Dataset

The dataset contains clinical data collected from patients, with the following features:

- **age**: Age in years  
- **sex**: Biological sex (1 = male, 0 = female)  
- **cp**: Chest pain type (0–3)  
- **trestbps**: Resting blood pressure (mm Hg)  
- **chol**: Serum cholesterol (mg/dl)  
- **fbs**: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)  
- **restecg**: Resting electrocardiographic results (0–2)  
- **thalach**: Maximum heart rate achieved  
- **exang**: Exercise-induced angina (1 = yes, 0 = no)  
- **oldpeak**: ST depression induced by exercise relative to rest  
- **slope**: Slope of peak exercise ST segment (0–2)  
- **ca**: Number of major vessels colored by fluoroscopy (0–3)  
- **thal**: Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect)  
- **target**: Presence of heart disease (1 = disease, 0 = no disease)

---

## 🧹 Data Cleaning & Exploration

- Checked for **null values** and **duplicates**, and cleaned the dataset accordingly.
- Performed exploratory data analysis:
  - Gender distribution of heart disease
  - Age distribution
  - Distribution of resting blood pressure (`trestbps`)
  - Serum cholesterol (`chol`) distribution
  - Correlation heatmap between features

---

## 📊 Model Building

- The data was split into **training** and **testing** sets.
- Two classification models were trained and evaluated:
  1. **Logistic Regression**
  2. **Decision Tree Classifier**

---

## ✅ Model Evaluation

Evaluation metrics used:
- **Accuracy**
- **F1 Score**

| Model              | Accuracy (%) | F1 Score (%) |
|-------------------|--------------|--------------|
| Logistic Regression |   _81.97%_ |   _83.08%_   |
| Decision Tree       |   _77.05%_ |   _78.79%_   |

→ Logistic Regression performed better and was selected for prediction.

---

## 🔍 Prediction Example

A random patient input was used to test the trained Logistic Regression model:

```python
input_data = pd.DataFrame(
    [[41, 0, 1, 130, 204, 0, 0, 172, 0, 1.4, 2, 0, 2]],
    columns=['age', 'sex', 'cp', 'trestbps', 'chol', 'fbs', 'restecg',
             'thalach', 'exang', 'oldpeak', 'slope', 'ca', 'thal']
)
prediction = model.predict(input_data)
