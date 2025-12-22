# 🔁 Telco_Churn_MLOps_Pipeline

🌐 Available in [English](README_EN.md)

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![DVC](https://img.shields.io/badge/MLOps-DVC-purple.svg)
![MLflow](https://img.shields.io/badge/Experiments-MLflow-lightblue.svg)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-black.svg)
![Status](https://img.shields.io/badge/Status-Portfolio-success.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

Este proyecto implementa un **pipeline completo y reproducible de Machine Learning** para la **predicción de churn en una empresa de telecomunicaciones**, aplicando prácticas modernas de **MLOps** mediante **DVC**, **MLflow**, **GitHub Actions** y **DagsHub**.

El foco está puesto en la **reproducibilidad, trazabilidad y automatización** del flujo de trabajo, desde la preparación de los datos hasta la evaluación del modelo.

---

## 🧰 Stack Tecnológico

- **Python (scikit-learn)** → entrenamiento y evaluación de modelos  
- **DVC** → versionado de datos, modelos y artefactos  
- **MLflow** → tracking de métricas y experimentos  
- **GitHub Actions** → validación automática del pipeline (CI)  
- **DagsHub** → almacenamiento remoto y servidor de MLflow  

---

## 🧭 Arquitectura del pipeline

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
Artefactos (modelos, métricas, gráficos)
```

El pipeline completo se ejecuta de forma reproducible mediante:

```bash
dvc repro
```

---

## 📂 Estructura del repositorio

```
Telco_Churn_MLOps_Pipeline/
│
├── .dvc/                      # Configuración de DVC
├── .github/workflows/ci.yml   # Pipeline de CI con GitHub Actions
├── data/                      # Raw / processed / prepared (vacío, runtime)
├── models/                    # Modelos entrenados (ignorados por Git)
├── params/                    # Configuración de modelos (YAML)
├── src/                       # Scripts del pipeline
├── dvc.yaml                   # Definición del pipeline
├── dvc.lock                   # Lockfile reproducible
├── requirements.txt
└── README.md
```

---

📂 **Carpeta de datos**  
Por razones de licencia y tamaño, los datasets utilizados no se incluyen en el repositorio público.  
La carpeta `data/` se genera automáticamente durante la ejecución del pipeline y se versiona mediante **DVC**.

---

## 🧰 Requisitos técnicos

- Python 3.11  
- Dependencias listadas en `requirements.txt`  
- DVC configurado con un remote (por ejemplo, DagsHub)

---

## 🚀 Ejecución

```bash
pip install -r requirements.txt
dvc repro
```

---

## 📊 Métricas evaluadas

- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC AUC  

Las métricas y artefactos se registran automáticamente en **MLflow**, permitiendo la comparación histórica de experimentos.

---

## 📝 Aprendizajes clave

- Diseño de pipelines de ML reproducibles con DVC.  
- Separación clara entre código, configuración y artefactos.  
- Integración de CI para validar workflows completos.  
- Tracking de experimentos con MLflow en entorno remoto.  
- Flujo de trabajo MLOps orientado a escenarios productivos.

---

📄 Licencia  
Este proyecto está bajo la licencia MIT.

---

✍️ Autor: Elías Fernández  
📧 Contacto: fernandezelias86@gmail.com  
🔗 LinkedIn: www.linkedin.com/in/eliasfernandez208