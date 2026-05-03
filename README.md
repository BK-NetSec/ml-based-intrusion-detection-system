# 🚨 Intrusion Detection System (IDS) using Machine Learning

## 📌 Overview
This project implements a Machine Learning-based Intrusion Detection System (IDS) using the UNSW-NB15 dataset. The system classifies network traffic into two categories:

- Normal
- Attack

It uses a Random Forest Classifier to detect malicious activity and includes basic Explainable AI (XAI) functionality to interpret predictions.

---

## ⚙️ Features
- End-to-end ML pipeline:
  - Data loading (Parquet format)
  - Data preprocessing & cleaning
  - Feature encoding
  - Feature scaling
  - Model training
  - Evaluation & visualization
- Binary classification (Normal vs Attack)
- Confusion matrix visualization
- Feature importance analysis
- Basic explainability for predictions
- Model export for deployment

---

## 📂 Dataset
The system uses the UNSW-NB15 dataset.

### Required Files:
- UNSW_NB15_training-set.parquet
- UNSW_NB15_testing-set.parquet

Make sure both files are in the project directory before running the script.

---

## 🧠 Model Details

- Algorithm: Random Forest Classifier  
- n_estimators: 100  
- max_depth: 20  
- random_state: 42  

---

## 🔄 Workflow

### 1. Data Acquisition
- Load training and testing datasets
- Merge for unified preprocessing

### 2. Data Preprocessing
- Remove unnecessary columns (attack_cat)
- Replace invalid values (- → 0)
- Encode categorical features using LabelEncoder
- Convert all data to numeric
- Handle missing values

### 3. Feature Engineering
- Split into features (X) and labels (y)
- Train-test split (80/20)
- Normalize data using StandardScaler

### 4. Model Training
- Train Random Forest on processed data

### 5. Evaluation
- Accuracy score
- Classification report
- Confusion matrix visualization

### 6. Visualization
- Heatmap of confusion matrix
- Top 15 most important features

### 7. Explainable AI (XAI)
- Function: explain_packet_decision(index)
- Shows:
  - Prediction (Normal/Attack)
  - Top 5 influencing features

### 8. Model Export
- Saved files:
  - final_ids_model.pkl
  - final_scaler.pkl

---

## 🚀 How to Run

### 1. Install Dependencies
pip install pandas numpy scikit-learn seaborn matplotlib joblib pyarrow

### 2. Run the Script
python your_script_name.py

---

## 📁 Project Structure
├── UNSW_NB15_training-set.parquet
├── UNSW_NB15_testing-set.parquet
├── main.py
├── final_ids_model.pkl
├── final_scaler.pkl
└── README.md

---

## ⚠️ Limitations

- Binary classification only
- No real-time detection
- Label encoding limitations
- Basic explainability only
- No hyperparameter tuning

---

## 🧠 Possible Improvements

- Use SHAP or LIME
- Multi-class classification
- Hyperparameter tuning
- Real-time detection
- Deploy with Flask or FastAPI

---

## 📌 Conclusion
This project demonstrates a solid foundation for building an IDS using machine learning.

---

## 👨‍💻 Author
Bahabelom kiros 
