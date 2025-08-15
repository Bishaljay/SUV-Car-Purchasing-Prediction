# 🚙 SUV Car Purchasing Prediction (Machine Learning)

## 📌 Problem Statement
The goal of this project is to predict whether a customer will purchase an SUV based on features such as **Age, Gender, and Estimated Salary**.  
This project demonstrates a simple **machine learning classification workflow** using Logistic Regression.

---

## 📂 Project Files
- `app.py` → Main **Streamlit app** file for interactive prediction  
- `suv_data.csv` → Dataset used for training and testing  
- `model.pkl` → Trained ML model saved with **pickle**  
- `requirements.txt` → Required Python packages  
- `README.md` → Project documentation  

---

## ⚙️ Setup Instructions
1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd suv-car-purchasing-prediction
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 Usage

### 1. Running the Model in Code

You can directly use the trained model:

```python
import pickle

# Load model
model = pickle.load(open("model.pkl", "rb"))

# Example input: Age=35, Gender=1 (Male), Salary=50000
prediction = model.predict([[35, 1, 50000]])

print("Will Purchase SUV?" , "Yes" if prediction[0] == 1 else "No")
```

### 2. Running with Streamlit App

Run the app:

```bash
streamlit run app.py
```

This will open a **web interface** where you can input Age, Gender, and Salary, and get prediction results.

---

## 📊 Example ML Workflow

The model uses **Logistic Regression** for classification:

```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(X_train, y_train)
```

Preprocessing steps include:

* Label Encoding for Gender (Male/Female → 1/0)
* Feature Scaling (StandardScaler) for Age and Salary

---

## 🎯 Usages

* Learn the basics of **classification models** in ML
* Understand **data preprocessing** (encoding + scaling)
* Build and deploy a **Streamlit web app**
* Serve as a **mini-project** for students, beginners, or hackathons

---

## 📝 Notes

* Dataset (`suv_data.csv`) must be placed in the correct folder
* Modify `app.py` to customize input fields
* You can replace Logistic Regression with **SVM, RandomForest, or XGBoost** to test performance

---

## 🔮 Future Enhancements

* Add more features (e.g., marital status, job role, income bracket)
* Implement multiple models and compare accuracy
* Deploy app to **Streamlit Cloud / Heroku / AWS**
