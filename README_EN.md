# 🔁 Telco_Churn_MLOps_Pipeline

🌐 Available in [Spanish](README.md)

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![DVC](https://img.shields.io/badge/MLOps-DVC-purple.svg)
![MLflow](https://img.shields.io/badge/Experiments-MLflow-lightblue.svg)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-black.svg)
![Status](https://img.shields.io/badge/Status-Portfolio-success.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

This project implements a **fully reproducible Machine Learning pipeline** for **customer churn prediction in a telecommunications company**, following modern **MLOps practices**.

The focus is on **reproducibility, traceability, and experimentation**, integrating **DVC**, **MLflow**, **GitHub Actions**, and **DagsHub** throughout the entire workflow: from data preparation to model comparison.

---

## 🧰 Tech Stack

- **Python / scikit-learn** → model training and evaluation  
- **DVC** → data, model, and artifact versioning  
- **MLflow** → experiment, parameter, and metric tracking  
- **GitHub Actions** → automated pipeline validation (CI)  
- **DagsHub** → remote storage and MLflow tracking server  

---

## 🧭 Pipeline Architecture

Raw data  
↓  
Preprocessing  
↓  
Feature Engineering  
↓  
Model Training → MLflow (params + metrics)  
↓  
Evaluation  
↓  
Artefactos (modelos, métricas)

El pipeline completo se ejecuta de forma reproducible mediante:

```bash
dvc repro
```

---

## 📊 Models and Experiments

Two supervised models were trained and compared:
- Logistic Regression
- Decision Tree

For Logistic Regression, the following values of the hyperparameter C were evaluated:
- C = 1
- C = 10
- C = 100

All experiments were tracked using MLflow, enabling systematic comparison of metrics and parameters.

**Evaluated Metrics**
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

---

## 📂 Repository Structure

```
Telco_Churn_MLOps_Pipeline/
│
├── .github/workflows/ci.yml   # GitHub Actions CI
├── data/                      # raw / processed / prepared (DVC)
├── params/                    # Model configuration (YAML)
├── src/                       # Pipeline scripts
├── metrics/                   # Evaluation metrics
├── models/                    # Trained models (DVC)
├── dvc.yaml                   # Pipeline definition
├── dvc.lock                   # Reproducible lockfile
├── requirements.txt
├── README.md
└── README_EN.md
```

---

## 🚀 Running the Pipeline

pip install -r requirements.txt
dvc repro

---

## 📝 Key Takeaways

- Design of reproducible ML pipelines with DVC
- Clear separation between code, configuration, and artifacts
- Model and experiment comparison using MLflow
- CI integration for full end-to-end workflow validation
- MLOps-oriented approach aligned with production scenarios

---

## 📄 License
This project is licensed under the MIT License.

---

✍️ Author: Elías Fernández
📧 Contact: fernandezelias86@gmail.com
🔗 LinkedIn: www.linkedin.com/in/eliasfernandez208