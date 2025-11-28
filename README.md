# 🌿 AyurSutra — Deep Learning Based Wellness Forecasting

AyurSutra is an AI-powered wellness prediction system that simulates, analyzes, and forecasts **daily wellness trends** in Ayurvedic therapy environments.  
Using synthetic multi-modal health data, LSTM forecasting, and ANN recovery classification, the project reimagines traditional wellness tracking through data-driven intelligence.

---

## 🚀 Features

- Generate **180,000+ synthetic Ayurvedic wellness records**
- Predict daily wellness using **LSTM time-series models**
- Classify patient recovery patterns using **ANN (~99% accuracy)**
- Model effects of therapies: *Abhyanga, Basti, Shirodhara, Nasya*
- Visualize vitals, symptoms, sleep, dosha patterns
- Capture short-term + long-term recovery behaviour

---

## 📁 Dataset Overview

A fully synthetic dataset generated programmatically.

Each record includes:

- `patient_id`, `day`
- `age`, `dosha` (Vata / Pitta / Kapha)
- `archetype` (A/B/C behavioural profile)
- `therapy` (4 options)
- `heart_rate`, `bp_systolic`
- `sleep_quality`
- `symptom_score`
- `wellness_score` (target)

**Dataset size:**

1000 patients × 180 days = 180,000 records


---

## ⚙️ Data Generation Logic

The synthetic engine simulates realistic Ayurvedic healing patterns using:

- Therapy-dependent physiological effects  
- Archetype-based variations in symptoms  
- Biological cycles using `sin()` and `cos()`  
- Random noise for natural variability  
- A composite wellness scoring formula (0–10)

This creates a high-quality, multi-modal time series suitable for deep learning.

---

## 🧽 Data Preprocessing

The preprocessing pipeline includes:

- Cleaning & filtering records  
- Encoding categorical values  
- Normalizing numeric features  
- Building **30-day rolling windows**  
- Splitting into train/validation/test  
- Visual analytics:
  - Heatmaps
  - Trend graphs  
  - Therapy effect curves  

---

## 📂 Project Structure

AyurSutra/
│
├── README.md # Project documentation
├── best_AyurSutra.ipynb # Main notebook: data generation, preprocessing, modelling
│
├── label_encoder_2.pkl # Label encoder for archetypes (A/B/C)
├── recovery_classifier_2.h5 # Trained ANN model for archetype classification
├── scaler_classifier_2.pkl # Scaler used for classifier input features
├── scaler_static_2.pkl # Scaler for static features (age, dosha, therapy, etc.)
├── scaler_ts_2.pkl # Scaler for time-series features for LSTM
├── wellness_predictor_lstm_2.h5 # Trained LSTM model for wellness prediction


## 📊 Key Results

### 🧠 **ANN Classification Model (Archetype Prediction)**

**Overall Metrics**

- **Accuracy:** 0.9920 (~99.20%)
- **F1 Score:** 0.9920 (~99.20%)

**Class-wise Performance**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| **A** | 1.00 | 0.99 | 1.00 | 14220 |
| **B** | 0.99 | 0.99 | 0.99 | 12240 |
| **C** | 0.99 | 0.99 | 0.99 | 9534 |

**Averages**

- **Macro Avg F1:** 0.99  
- **Weighted Avg F1:** 0.99  

✔ Near-perfect classification  
✔ ANN model clearly distinguishes all three recovery archetypes  


---

### 📈 **LSTM Regression Model (Wellness Forecasting)**

| Metric | Score |
|--------|--------|
| **MAE** | 0.5886 |
| **RMSE** | 0.7367 |
| **R² Score** | 0.5189 |

✔ Low prediction error  
✔ R² > 0.5 indicates strong variance capture  
✔ Solid baseline for further improvements  



The system successfully learns:

- Therapy influence on wellness  
- Dosha-based patterns  
- Symptom interactions  
- Cumulative healing trajectories  

---

## 📈 Visual Insights

The notebook generates:

- Therapy impact visualizations  
- Heart rate & blood pressure trends  
- Symptom vs wellness relationships  
- Forecast vs actual curves  
- Correlation heatmaps  
- Patient archetype clusters  

These visuals make the wellness modelling easy to interpret.

---

## 🚀 Deployment (Streamlit App)

This project is deployed using **Streamlit**, providing an interactive interface for:

- Uploading patient data  
- Predicting wellness score using the LSTM model  
- Predicting recovery archetype using the ANN classifier  
- Visualizing trends and wellness insights  

## 💻 Tech Stack

- Python 3
- LSTM, ANN
- TensorFlow / Keras  
- NumPy, Pandas  
- Matplotlib, Seaborn
- Streamlit

---

---

## 🔮 Future Enhancements

- Integrate real Ayurvedic clinical datasets  
- Add Transformer-based forecasting  
- Mobile-friendly real-time wellness tracker  
- Include sensor data (HRV, sleep monitors)  
- Multi-output prediction (stress, fatigue, energy score)

---

## 👤 Author

**Faiz Ali**,
**Yashwanth Reddy**,
**Navadeep**

---


