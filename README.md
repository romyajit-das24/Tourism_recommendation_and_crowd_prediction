# 🌍 Smart Tourist Recommendation System with Crowd Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue.svg"/>
  <img src="https://img.shields.io/badge/Machine%20Learning-Random%20Forest-green"/>
  <img src="https://img.shields.io/badge/Status-Completed-success"/>
  <img src="https://img.shields.io/badge/Accuracy-78%25-orange"/>
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-yellow"/>
</p>

---

## 📌 Project Overview

An **AI-powered Tourist Recommendation System** enhanced with a **Crowd Prediction Model** that helps users discover places while avoiding overcrowding.

👉 The system recommends destinations and predicts crowd levels (**Low / Medium / High**) based on time, location, and contextual features.

---

## 🚀 Features

* 🌍 Tourist place recommendations
* 👥 Crowd level prediction
* 📊 Data-driven insights
* 🧠 Machine Learning integration
* ⚡ Realistic feature engineering

---

## 🧠 System Architecture

```
User Input (location, preferences, time)
        ↓
Tourist Recommendation Model
        ↓
Crowd Prediction Model
        ↓
Final Output:
Recommended Places + Crowd Level
```

---

## 📂 Dataset

### 🔹 Tourism Dataset

Includes:

* `destination_name` (place)
* `state`, `region`
* `popularity_score` (used as rating)
* Travel-related metadata

### 🔹 Crowd Dataset (Generated)

Extended dataset with:

* `time`, `day`, `weekend`
* Engineered features (`is_peak`, `weekend_peak`)
* Target: `crowd` (Low / Medium / High)

---

## 🔧 Feature Engineering

| Feature           | Description                       |
| ----------------- | --------------------------------- |
| `is_peak`         | Identifies peak hours (afternoon) |
| `high_popularity` | High-rated destinations           |
| `weekend_peak`    | Combined weekend + peak effect    |

---

## 🤖 Machine Learning Model

* **Algorithm:** Random Forest Classifier
* **Why:**

  * Handles mixed data types
  * Robust performance
  * Good generalization

---

## 📊 Model Performance

| Stage         | Accuracy              |
| ------------- | --------------------- |
| Initial Model | ~99% ❌ (data leakage) |
| Final Model   | ~78% ✅ (realistic)    |

> ⚠️ Removed `busy_score` to eliminate **data leakage**

---

## 📈 Exploratory Data Analysis (EDA)

* 📊 Crowd distribution
* ⏰ Time vs Crowd patterns
* 📅 Weekend impact
* 📌 Feature importance

---

## 🧪 Prediction Example

```python
predict_crowd({
    "place": "Goa Beach",
    "state": "Goa",
    "region": "West",
    "rating": 85,
    "time": "afternoon",
    "day": "Sunday",
    "weekend": 1
})
```

### ✅ Output:

```
High
```

---

## 💾 Model Saving

```python
joblib.dump(model, "crowd_model.pkl")
joblib.dump(X.columns, "model_columns.pkl")
```

---

## ⚙️ Installation & Setup

```bash
git clone https://github.com/your-username/tourism-crowd-prediction.git
cd tourism-crowd-prediction
pip install -r requirements.txt
```

---

## ▶️ How to Run

1. Upload dataset in Google Colab
2. Run preprocessing & feature engineering
3. Train the model
4. Save model files
5. Run prediction function

---

## 🔮 Future Improvements

* 🌐 Real-time APIs integration
* 🗺️ Google Maps Popular Times
* 📱 Streamlit Web App
* ☁️ Cloud Deployment
* 🧠 Deep Learning models (LSTM)

---

## 🏆 Key Highlights

* ✔️ End-to-end ML pipeline
* ✔️ Solved data leakage problem
* ✔️ Applied feature engineering
* ✔️ Built scalable prediction system

---

## 🛠 Tech Stack

* Python
* Pandas
* Scikit-learn
* Matplotlib
* Joblib
* Google Colab

---

## 👨‍💻 Author

**Romyajit Das**

---

## ⭐ Show Your Support

If you like this project, give it a ⭐ on GitHub!


