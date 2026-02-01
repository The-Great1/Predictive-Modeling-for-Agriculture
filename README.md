# 🌾 Predictive Modeling for Agriculture

### Sowing Success: How Machine Learning Helps Farmers Select the Best Crops

## 📌 Project Overview

Choosing the right crop to plant is one of the most important decisions a farmer makes each season. Soil testing provides valuable insights into soil health, but measuring every possible metric can be **expensive and time-consuming**.

In this project, machine learning is used to help farmers **predict the optimal crop** for a field using a small set of essential soil measurements. Additionally, the project identifies the **single most important soil feature** for making accurate predictions — helping farmers prioritize what to measure when resources are limited.

---

## 🎯 Objectives

* Build a **multi-class classification model** to predict the optimal crop for a field.
* Evaluate predictive performance using **macro-averaged F1 score**.
* Identify the **most predictive soil feature** for crop selection.

---

## 📂 Dataset

**File:** `soil_measures.csv`
Each row represents soil measurements from a specific field.

### 🧾 Feature Description

| Feature | Description                                      |
| ------- | ------------------------------------------------ |
| `N`     | Nitrogen content ratio in the soil               |
| `P`     | Phosphorous content ratio in the soil            |
| `K`     | Potassium content ratio in the soil              |
| `ph`    | Soil pH value                                    |
| `crop`  | Optimal crop for the field (**target variable**) |

---

## 📊 Dataset Summary

* **Total samples:** 2,200
* **Number of crops:** 22
* **Problem type:** Multi-class classification
* **Target:** `crop`

---

## 🛠️ Methodology

### 1️⃣ Data Exploration

* Inspected feature distributions and data types
* Verified class balance and absence of missing values

### 2️⃣ Data Preprocessing

* Encoded categorical crop labels using **Label Encoding**
* Split data into training and test sets (80/20 split) with stratification

### 3️⃣ Model Selection

* Used **Multinomial Logistic Regression** for multi-class classification

### 4️⃣ Feature Importance Analysis

* Trained separate models using **one feature at a time**
* Evaluated each model using:

  * **Macro F1 Score**
  * Training accuracy
  * Test accuracy
* Compared performance to identify the most predictive soil metric

---

## 📈 Model & Metrics

* **Model:** Multinomial Logistic Regression
* **Evaluation Metric:** Macro-averaged F1 Score
  (chosen to account for class imbalance across 22 crops)

---

## 🏆 Results

### 🔑 Best Predictive Feature

| Feature             | Macro F1 Score |
| ------------------- | -------------- |
| **Potassium (`K`)** | **0.283**      |

Potassium (`K`) emerged as the **single most important soil feature** for predicting the optimal crop, outperforming nitrogen, phosphorous, and pH when used independently.

---

## 🌱 Key Insights

* Soil nutrients vary significantly in predictive power for crop selection.
* Potassium plays a dominant role in distinguishing between crop types.
* Machine learning can guide **cost-effective soil testing strategies** by identifying which measurements matter most.

---

## 📦 Tech Stack

* **Python 3**
* **pandas**
* **scikit-learn**
