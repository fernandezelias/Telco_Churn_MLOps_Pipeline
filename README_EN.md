# 🔁 Telco_Churn_MLOps_Pipeline

🌐 Disponible en [Español](README.md)

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![DVC](https://img.shields.io/badge/MLOps-DVC-purple.svg)
![MLflow](https://img.shields.io/badge/Experiments-MLflow-lightblue.svg)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-black.svg)
![Status](https://img.shields.io/badge/Status-Portfolio-success.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

This project implements a **fully reproducible Machine Learning pipeline** for **telecom customer churn prediction**, applying modern **MLOps practices** using **DVC**, **MLflow**, **GitHub Actions**, and **DagsHub**.

The main focus is on **reproducibility, traceability, and automation**, from data preparation to model evaluation.

---

## 🧰 Tech Stack

- **Python (scikit-learn)** → model training and evaluation  
- **DVC** → data and model versioning  
- **MLflow** → experiment and metric tracking  
- **GitHub Actions** → CI pipeline validation  
- **DagsHub** → remote storage and MLflow server  

---

## 🧭 Pipeline Architecture

```
Raw data
   │
   ▼
Preprocessing
   │
   ▼
Feature Engineering
   │
   ▼
Model Training  ──► MLflow (params + metrics)
   │
   ▼
Evaluation
   │
   ▼
Artifacts (models, metrics, plots)
```

The entire workflow is executed reproducibly via:

```bash
dvc repro
```

---

## 📂 Repository Structure

```
Telco_Churn_MLOps_Pipeline/
│
├── .dvc/                      # DVC configuration
├── .github/workflows/ci.yml   # GitHub Actions CI
├── data/                      # Runtime data folders (empty)
├── models/                    # Trained artifacts (Git-ignored)
├── params/                    # Model configuration (YAML)
├── src/                       # Pipeline scripts
├── dvc.yaml                   # Pipeline definition
├── dvc.lock                   # Reproducible lockfile
├── requirements.txt
└── README.md
```

---

📂 **Data folder**  
Datasets are not included in the public repository due to licensing and size constraints.  
The `data/` directory is generated at runtime and versioned using **DVC**.

---

## 🧰 Technical Requirements

- Python 3.11  
- Dependencies listed in `requirements.txt`  
- DVC configured with a remote (e.g., DagsHub)

---

## 🚀 Execution

```bash
pip install -r requirements.txt
dvc repro
```

---

## 📊 Evaluated Metrics

- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC AUC  

All metrics and artifacts are logged in **MLflow**, enabling transparent experiment comparison.

---

## 📝 Key Learnings

- Designing reproducible ML pipelines with DVC.  
- Clear separation between code, configuration, and artifacts.  
- CI integration for full workflow validation.  
- Experiment tracking with remote MLflow.  
- Production-oriented MLOps workflows.

---

📄 License  
This project is released under the MIT License.

---

✍️ Author: Elías Fernández  
📧 Contact: fernandezelias86@gmail.com  
🔗 LinkedIn: www.linkedin.com/in/eliasfernandez208