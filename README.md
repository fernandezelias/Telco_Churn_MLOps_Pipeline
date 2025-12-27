# 🔁 Telco Churn MLOps Pipeline  

🌐 Available in [English](README_EN.md)

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![DVC](https://img.shields.io/badge/MLOps-DVC-purple.svg)
![MLflow](https://img.shields.io/badge/Experiments-MLflow-lightblue.svg)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-black.svg)
![Status](https://img.shields.io/badge/Status-Portfolio-success.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

Este proyecto implementa un **pipeline completo y reproducible de Machine Learning** para la **predicción de churn en una empresa de telecomunicaciones**, aplicando prácticas modernas de **MLOps**.

El foco está puesto en la **reproducibilidad, trazabilidad y automatización** del flujo de trabajo, desde la preparación de los datos hasta la evaluación del modelo, integrando **DVC**, **MLflow**, **GitHub Actions** y **DagsHub**.

---

## 🧰 Stack Tecnológico

- **Python / scikit-learn** → entrenamiento y evaluación de modelos  
- **DVC** → versionado de datos, modelos y artefactos  
- **MLflow** → tracking de métricas, parámetros y experimentos  
- **GitHub Actions** → validación automática del pipeline (CI)  
- **DagsHub** → almacenamiento remoto y servidor de MLflow  

---

## 🧭 Arquitectura del pipeline

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

## 📊 Modelos y Experimentos

Se entrenaron y compararon dos modelos supervisados:
- Logistic Regression
- Decision Tree

Para el modelo Logistic Regression se evaluaron los siguientes valores del hiperparámetro C:
- C = 1
- C = 10
- C = 100

Los experimentos fueron registrados con MLflow, permitiendo comparar métricas y parámetros de forma sistemática.

**Métricas evaluadas**
- Accuracy
- Precision
- Recall
- F1-score
- ROC AUC

---

## 📂 Estructura del repositorio

```
Telco_Churn_MLOps_Pipeline/
│
├── .github/workflows/ci.yml   # CI con GitHub Actions
├── data/                      # raw / processed / prepared (DVC)
├── params/                    # Configuración de modelos (YAML)
├── src/                       # Scripts del pipeline
├── metrics/                   # Métricas de evaluación
├── models/                    # Modelos entrenados (DVC)
├── dvc.yaml                   # Definición del pipeline
├── dvc.lock                   # Lockfile reproducible
├── requirements.txt
├── README.md
└── README_EN.md
```

---

## 🚀 Ejecución del pipeline

pip install -r requirements.txt
dvc repro

---

## 📝 Aprendizajes clave

- Diseño de pipelines de ML reproducibles con DVC
- Separación clara entre código, configuración y artefactos
- Comparación de modelos y experimentos con MLflow
- Integración de CI para validar workflows completos
- Enfoque MLOps orientado a escenarios productivos reales

---

## 📄 Licencia
Este proyecto está bajo la licencia MIT.

---

✍️ **Autor:** Elías Fernández  
📧 **Contacto:** fernandezelias86@gmail.com  
🔗 **LinkedIn:** https://www.linkedin.com/in/eliasfernandez208