# Graduate Admission Predictor 🎓

A Deep Learning-based regression model built using **TensorFlow/Keras** and **Scikit-Learn** to predict a student's probability of gaining admission into a graduate program based on academic credentials and research profile. 

## 📌 Repository Description   

> **Short Description :**  
> *A Deep Learning regression pipeline using TensorFlow/Keras to predict graduate university admission probability based on GRE, TOEFL, CGPA, and profile strength.*  

---

## 📂 Project Structure 

├── dataset/
│   └── Admission_Predict_Ver1.1.csv  
├── notebooks/
│   └── admission_prediction.ipynb    
├── README.md                          
└── requirements.txt                  


---

## 📊 Dataset Overview

The dataset used in this project is the **Graduate Admissions Dataset** from Kaggle. It contains various parameters considered crucial for application to Master's programs: 

- **GRE Score** (out of 340)
- **TOEFL Score** (out of 120)
- **University Rating** (out of 5)
- **SOP** – Statement of Purpose strength (out of 5)
- **LOR** – Letter of Recommendation strength (out of 5)
- **CGPA** (out of 10)
- **Research Experience** (0 or 1)
- **Chance of Admit** *(Target Variable)* – Ranges from 0 to 1

---

## 🛠️ Tech Stack & Libraries

- **Language:** Python 3.x
- **Deep Learning Framework:** TensorFlow, Keras
- **Machine Learning & Preprocessing:** Scikit-Learn (`MinMaxScaler`, `train_test_split`, `r2_score`)
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib

---

## ⚙️ Model Architecture

The model is built as a Multilayer Perceptron (MLP) using Keras Sequential API:

1. **Input Layer:** `Input(shape=(7,))` for normalized academic features.
2. **Hidden Layer 1:** `Dense(7, activation='relu')`
3. **Hidden Layer 2:** `Dense(7, activation='relu')`
4. **Output Layer:** `Dense(1, activation='linear')` for continuous probability estimation.


   ---

## 🚀 Step-by-Step Pipeline

1. **Data Cleaning:** Removed non-predictive identifiers (`Serial No.`).
2. **Train-Test Split:** Partitioned dataset into 80% training set and 20% test set (`random_state=1`).
3. **Normalization:** Applied `MinMaxScaler` on training features to standardise values between 0 and 1.
4. **Model Training:** Trained over 100 epochs using `Adam` optimizer and `Mean Squared Error` loss with a 20% validation split.
5. **Evaluation:** Evaluated model performance on unseen test data using $R^2$ score.

---

## 📈 Performance & Results

- **Training Epochs:** 100
- **Loss Metric:** Mean Squared Error (MSE)
- **Test Set $R^2$ Score:** `~0.809` (Explains ~80.9% of the target variance)

---
