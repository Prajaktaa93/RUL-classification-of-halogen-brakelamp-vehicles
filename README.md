# 🚗 Brake Lamp RUL Prediction (Predictive Maintenance)

## 📌 Overview
This project focuses on predicting the **Remaining Useful Life (RUL) stage** of automotive brake lamps using machine learning.  
Instead of predicting exact RUL (which is unrealistic in real-world scenarios), the problem is reformulated into a **classification task**:
- Healthy
- Warning
- Critical

---

## 🎯 Objective
To build a **realistic predictive maintenance system** that:
- Uses only real-time sensor data  
- Avoids data leakage  
- Accurately detects early failure signals  

---

## ⚙️ Methodology

### 🔹 Data Processing
- Cleaned and preprocessed sensor dataset  
- Handled missing values  
- Encoded categorical features  
- Removed leakage-prone features (e.g., `Lifetime`)  

### 🔹 Temporal Strategy
- Performed **lamp-wise train-test split** to simulate real-world unseen devices  
- Ensured no temporal leakage  

### 🔹 Feature Engineering
- Resistance-based degradation features  
- Power deviation and change rates  
- Time-based operational features  

### 🔹 Modeling
- Used **XGBoost Classifier**  
- Applied **class weighting** to handle class imbalance  
- Focused on improving **critical failure detection**  

---

## 📊 Results

| Metric | Value |
|------|------|
| Accuracy | ~80% |
| Critical Recall | ~55% |
| Healthy Recall | ~100% |

✔ Significant improvement in failure detection  
✔ Realistic and deployable model  

---

## 📈 Key Insights
- **Power Deviation** is the strongest indicator of failure  
- **Resistance Change** reflects physical degradation  
- Electrical parameters (Current, Voltage) capture instability  
- Model learns true degradation patterns without data leakage  

---

## 📊 Visualizations

### Confusion Matrix
![Confusion Matrix](images/confusion_matrix.png)

### Feature Importance
![Feature Importance](images/FI_RUL.png)

---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/prajaktaa93/Brake-Lamp-RUL-Prediction.git
cd Brake-Lamp-RUL-Prediction

# Install dependencies
pip install -r requirements.txt
