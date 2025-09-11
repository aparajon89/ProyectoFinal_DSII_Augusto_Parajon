# 🌦️ ProyectoDSII – Augusto Parajón  

**Análisis climático de San Miguel de Tucumán para anticipar picos de frío y calor, optimizar stock de climatizadores y mejorar campañas de venta usando EDA, PCA, clustering y modelos de Machine Learning en Python.**  

**📚 Entrega Final – Data Science II**  
**👤 Autor:** Augusto Parajón  
**📅 Fecha:** Septiembre 2025  

---

## 📖 Descripción del Proyecto  
En este trabajo se analiza el comportamiento climático de **San Miguel de Tucumán** entre el 1 de enero de 2005 y el 31 de julio de 2025, con el objetivo de:  
- Anticipar **picos de frío y calor**.  
- Optimizar la **gestión de inventarios** de productos de climatización (ventiladores, aires acondicionados, estufas).  
- Mejorar el diseño de **campañas comerciales** en Oscar Barbieri S.A.  

El proyecto sigue la metodología **CRISP-DM**, integrando desde el análisis exploratorio hasta el modelado predictivo con Machine Learning.  

---

## 🎯 Objetivos  
- Modelar la situación como un **problema de clasificación de extremos climáticos**.  
- Entrenar y evaluar múltiples algoritmos de Machine Learning.  
- Aplicar técnicas de optimización de hiperparámetros.  
- Seleccionar el mejor modelo según métricas de clasificación.  
- Traducir los hallazgos en **insights accionables para el negocio**.  

---

## 🗂 Dataset  
- **Fuente:** [API Open-Meteo](https://open-meteo.com)  
- **Periodo:** 01/01/2005 – 31/07/2025  
- **Ubicación:** San Miguel de Tucumán, Argentina  
- **Variables principales:**  
  - Temperaturas mín/máx y temperatura aparente  
  - Precipitación, viento, humedad, radiación solar  
- **Target:** extremos climáticos (olas de calor/frío)  

---

## 🔎 Metodología  
1. **Adquisición de datos** → descarga desde API y exportación a CSV.  
2. **Wrangling y limpieza** → control de nulos, duplicados y plausibilidad de rangos.  
3. **EDA** → hipótesis H1–H6, estacionalidad, persistencia, percentiles vs. umbrales, clustering.  
4. **Ingeniería de atributos** → features temporales, flags de extremos, lags, PCA y clustering.  
5. **Modelado y validación** → entrenamiento de múltiples modelos + validación con `TimeSeriesSplit`.  
6. **Optimización** → `GridSearchCV` y `RandomizedSearchCV`.  
7. **Interpretabilidad** → coeficientes de Logistic Regression y análisis con **SHAP**.  
8. **Conclusiones** → aplicación a decisiones de inventario, logística y campañas.  

---

## 📊 Resultados  
- **Mejor modelo:** Logistic Regression (F1 macro = 0.725).  
- **Hallazgos clave:**  
  - La **temperatura aparente** supera en predictividad a la temperatura seca.  
  - Los **percentiles** son más robustos que los umbrales absolutos.  
  - Los **clusters** identifican perfiles climáticos diferenciados.  
- **Aplicación en negocio:** permite anticipar picos de demanda, planificar inventario y optimizar campañas comerciales.  

---

## ⚙️ Requisitos  
Ejecutar en **Google Colab** o entorno local con Python 3.10+.  

**Librerías principales:**  
`numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`, `shap`  

###Instalación rápida en Colab:  

!pip install numpy pandas scikit-learn xgboost shap seaborn matplotlib --quiet

## 🚀 Ejecución

### Clonar el repositorio:

git clone https://github.com/aparajon89/ProyectoFinal_DSII_Augusto_Parajon.git
cd ProyectoFinal_DSII_Augusto_Parajon


### Abrir la notebook en Jupyter o Colab:
ProytectoFinal_DSII_Augusto_Parajon.ipynb

Ejecutar todas las celdas con Restart & Run All.

## 📂 Estructura del Repositorio
├── ProytectoFinal_DSII_Augusto_Parajon.ipynb   # Notebook principal
├── clima_tucuman_historico.csv                 # Dataset generado
├── presentacion_final.pdf                      # Presentación ejecutiva
└── README.md                                   # Este archivo

## 👤 Autor

Augusto Parajón
Proyecto Final – Data Science II
