# 🎓 Student Burnout Prediction using Random Forest Classification

## 📌 Project Overview

This project aims to predict student burnout levels using the **Random Forest Classification Algorithm**. Burnout among students is a growing concern due to academic pressure, lifestyle imbalance, and stress. This model helps in early identification of burnout levels so that preventive measures can be taken.

## 🎯 Objective

* To build a machine learning model that predicts student burnout
* To analyze key factors influencing burnout such as study habits, sleep, and stress
* To assist in early detection and improve student well-being

## 📊 Dataset Description

* **Dataset Type:** Tabular Data
* **Domain:** Education / Healthcare
* **Number of Samples:** (Specify based on your dataset)
* **Features (Inputs):**

  * Study Hours
  * Sleep Duration
  * Stress Level
  * Physical Activity
  * Screen Time
  * Academic Performance
* **Target Variable:** Burnout Level (Low / Medium / High)

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib / Seaborn

## 🤖 Machine Learning Model

* **Algorithm:** Random Forest Classifier
* Ensemble learning technique combining multiple decision trees
* Reduces overfitting and improves prediction accuracy
* Handles both numerical and categorical data efficiently

## ⚙️ Project Workflow

1. **Data Collection**
2. **Data Preprocessing**

   * Handling missing values
   * Encoding categorical variables
   * Feature scaling
3. **Model Training** using Random Forest
4. **Model Evaluation**

   * Accuracy Score
   * Confusion Matrix
5. **Data Visualization**

## 📈 Results

* The model achieved good accuracy in predicting burnout levels
* Stress level and sleep duration were major contributing factors
* Random Forest provided stable and reliable performance

## 🚀 Future Enhancements

* Use real-time and larger datasets
* Implement advanced models like XGBoost and Deep Learning
* Deploy as a web application using Flask or Streamlit
* Integrate personalized recommendations for students

## 📂 Project Structure

```
├── dataset.csv
├── main.py
├── model.pkl
├── README.md
```

## ▶️ How to Run the Project

1. Clone the repository

```
git clone https://github.com/your-username/student-burnout-prediction.git
```

2. Navigate to the project folder

```
cd student-burnout-prediction
```

3. Install required libraries

```
pip install pandas numpy scikit-learn matplotlib seaborn
```

*(or create a requirements.txt file and use: `pip install -r requirements.txt`)*

4. Run the Python file

```
python main.py
```

## 📜 Main Python Implementation

Below is a simplified version of the core model implementation used in this project:

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, confusion_matrix

# Load dataset
data = pd.read_csv('dataset.csv')

# Features and target
X = data.drop('Burnout_Level', axis=1)
y = data['Burnout_Level']

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Model training
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Predictions
y_pred = model.predict(X_test)

# Evaluation
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)
print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
```

## 📌 Conclusion

This project demonstrates how machine learning can be used to analyze student behavior and predict burnout levels effectively. It highlights the importance of maintaining a balanced lifestyle and provides a foundation for further research in student mental health prediction.
