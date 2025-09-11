Proyecto Final – Data Science II

Análisis Climático Aplicado a la Planificación Comercial en Retail

📌 Descripción

Este proyecto busca anticipar la demanda de productos de climatización en Oscar Barbieri S.A. mediante el análisis de datos climáticos históricos de San Miguel de Tucumán (2005–2025) obtenidos desde la API Open-Meteo.

Se utilizó la metodología CRISP-DM, integrando análisis exploratorio, ingeniería de atributos y modelos de Machine Learning para predecir extremos climáticos que impactan en las ventas de calefacción y refrigeración.

🎯 Objetivos

Retomar el trabajo exploratorio previo y sumarle modelos de Machine Learning.

Modelar la situación como un problema de clasificación de extremos climáticos.

Entrenar y evaluar distintos algoritmos (Logistic Regression, Random Forest, Gradient Boosting, SVC, XGBoost, KNN).

Aplicar técnicas de optimización de hiperparámetros.

Seleccionar el modelo con mejor desempeño según métricas de clasificación.

Traducir los hallazgos en insights aplicables a la planificación comercial y logística en retail.

🗂 Dataset

Fuente: API Open-Meteo (https://open-meteo.com
).

Periodo: 01/01/2005 – 31/07/2025.

Ubicación: San Miguel de Tucumán, Argentina.

Variables principales: temperaturas mín/máx, temperatura aparente, precipitaciones, viento, humedad, radiación solar.

Target: etiqueta de extremos climáticos (olas de calor/frío).

🔎 Metodología

Adquisición de datos: descarga desde la API y exportación a CSV.

Wrangling y limpieza: control de nulos, duplicados y plausibilidad de rangos.

EDA: hipótesis H1–H6, estacionalidad, persistencia, percentiles vs. umbrales y clustering multivariado.

Ingeniería de atributos:

Variables temporales (día, mes, estación, transformaciones trigonométricas).

Flags de extremos.

Persistencia (lags y rolling means).

PCA y clustering como features adicionales.

Modelado y validación: entrenamiento de modelos base y avanzados con TimeSeriesSplit.

Optimización: GridSearchCV y RandomizedSearchCV.

Interpretabilidad: coeficientes de Logistic Regression y análisis SHAP.

Conclusiones: aplicación a decisiones de inventario, logística y campañas comerciales.

📊 Resultados

Mejores modelos: Logistic Regression y Gradient Boosting (según F1 y ROC-AUC).

Hallazgos clave:

La temperatura aparente supera en predictividad a la temperatura seca.

Percentiles más robustos que umbrales absolutos.

Los clusters muestran perfiles climáticos diferenciados.

Aplicación en negocio: anticipación de picos de demanda, planificación logística y optimización comercial.

⚙️ Requisitos

Ejecutar en Google Colab o entorno local con Python 3.10+.
Librerías principales:

numpy, pandas, matplotlib, seaborn

scikit-learn, xgboost, shap

Instalación rápida en Colab:

!pip install numpy pandas scikit-learn xgboost shap seaborn matplotlib --quiet

🚀 Ejecución

Clonar el repositorio:

git clone https://github.com/aparajon89/ProyectoFinal_DSII_Augusto_Parajon.git
cd ProyectoFinal_DSII_Augusto_Parajon


Abrir la notebook en Jupyter o Colab:
ProytectoFinal_DSII_Augusto_Parajon.ipynb

Ejecutar todas las celdas con Restart & Run All.

📂 Estructura del repositorio
├── ProytectoFinal_DSII_Augusto_Parajon.ipynb   # Notebook principal
├── clima_tucuman_historico.csv                 # Dataset generado
└── README.md                                   # Este archivo

👤 Autor

Augusto Parajón – Proyecto Final, Data Science II.
