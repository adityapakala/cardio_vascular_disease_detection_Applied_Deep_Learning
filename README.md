# cardio_vascular_disease_detection_Applied_Deep_Learning

# 🧠 Cardiovascular Disease Prediction using Neural Networks

This project was completed for the course **BUAN 6382: Applied Deep Learning** at the University of Texas at Dallas. We developed and trained a neural network from scratch to classify the risk of cardiovascular disease using clinical patient data.

---

## 📁 Project Files

- `cardio_nn.ipynb`: Main Colab notebook with all code, training outputs, evaluation metrics, and explainability.
- `cardio_train.csv`: The dataset used (sourced from Kaggle).
- `README.md`: This file — contains setup and reproduction instructions.
- `report.pdf` / `presentation.pdf`: Final summary of methodology, results, and key findings.

---

## 🧩 Dataset

- **Source**: [Kaggle - Cardiovascular Disease Detection](https://www.kaggle.com/datasets/bhadaneeraj/cardio-vascular-disease-detection)
- **Size**: ~70,000 records
- **Features**: Age, gender, blood pressure, cholesterol, glucose, physical activity, smoking/alcohol habits, etc.
- **Target**: `cardio` (1 = disease present, 0 = no disease)

---

## 🛠️ How to Run (Google Colab Instructions)

1. Open the `cardio_nn.ipynb` notebook in **Google Colab**.
2. Make sure to upload `cardio_train.csv` when prompted.
3. **Important**: Turn off GPU in Colab before running SHAP explainability (optional step).
4. Run all cells sequentially to train the model, evaluate it, and generate visual outputs.

---

## 🧠 Neural Network Design

- **Framework**: TensorFlow / Keras (via Colab)
- **Architecture**:
  - Input: 11 features
  - Hidden Layers: Dense(64) → Dropout(0.3) → Dense(32) → Dropout(0.2)
  - Output: Dense(1, sigmoid)
- **Regularization**:
  - Dropout Layers
  - L2 Weight Decay
  - EarlyStopping (patience=5)
- **Optimizer**: Adam
- **Loss**: Binary Crossentropy

---

## 📊 Model Performance

- **Validation Accuracy**: ~73.2%
- **Test Accuracy**: **74%**
- **F1 Scores**:
  - No Disease: 0.74–0.75
  - Disease: 0.73
- **Balanced precision & recall**, robust generalization

---

## 🔎 Explainability with SHAP

- Used SHAP (SHapley Additive exPlanations) to interpret model decisions.
- **Top Features Influencing Predictions**:
  - `ap_hi` (Systolic BP)
  - `age`
  - `cholesterol`
- SHAP plots confirm the model aligns well with medical risk factors.

---

## 📌 Key Insights

- High blood pressure, age, and cholesterol were most predictive of cardiovascular disease.
- Regularization improved model robustness without sacrificing accuracy.
- SHAP explainability adds interpretability crucial for real-world medical applications.

---

## 🧾 Reproducibility Checklist

- ✅ All code and outputs included in Colab
- ✅ Random seeds fixed for consistent train-test splits
- ✅ SHAP analysis included with visual plots
- ✅ Classification report and confusion matrix plotted

---

## 👥 Authors

Aditya Pakala and Team  
MS in Information Technology and Management  
The University of Texas at Dallas

---

## 📬 Questions?

Please contact the course instructor or TA if you have any issues running the notebook or reproducing results.
