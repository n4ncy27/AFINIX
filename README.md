
# AFINIX - Sistema Inteligente de Compatibilidad con Machine Learning

![Banner del Proyecto](banner%20(2).jpeg)

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Sistema avanzado de predicción de compatibilidad basado en Machine Learning**

[Autores](#autores) • [Objetivo](#objetivo) • [Dataset](#dataset) • [Modelos](#modelos-y-técnicas) • [Enlaces](#enlaces-del-proyecto)

</div>

---

<div align="center">
### *"La compatibilidad es la chispa que convierte el encuentro en destino"*

</div>

---

## Tabla de Contenido

- [Autores](#autores)
- [Objetivo](#objetivo)
- [Dataset](#dataset)
- [Modelos y Técnicas](#modelos-y-técnicas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Resultados](#resultados)
- [Enlaces del Proyecto](#enlaces-del-proyecto)
- [Instalación y Uso](#instalación-y-uso)

---

## Autores

**Johan Santiago Rojas Naranjo** (2225005), **Leyson David Celis Acelas** (2225002), **Nancy Liliana Saenz Moreno** (2224510)

---

## Objetivo

> **Predecir el nivel de afinidad entre personas mediante Machine Learning, evaluando compatibilidad multidimensional en hábitos, creencias, intereses y rasgos de personalidad para generar recomendaciones precisas y significativas.**

Ante las limitaciones de los métodos tradicionales de filtrado, **AFINIX** implementa un sistema avanzado que permite evaluar la compatibilidad entre personas de manera integral, superando las restricciones de los algoritmos convencionales.

---

## Dataset

### **OkCupid Profiles Dataset**

- **Fuente:** OkCupid Dating Profiles
- **Tamaño:** ~60,000 perfiles de usuarios
- **Variables:** 31 características originales (29 después de limpieza)
- **Características principales:**
  - Demográficas: edad, altura, sexo, orientación
  - Estilo de vida: alimentación, bebidas, drogas, tabaco
  - Preferencias: educación, trabajo, mascotas, religión, signo zodiacal
  - Estado: relación actual

**Descargar Dataset:**
- [Kaggle - OkCupid Profiles](https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles)
- [GitHub - Dataset Mirror](https://github.com/rudeboybert/JSE_OkCupid)

### Preprocesamiento:
- Eliminación de ensayos (essay0-essay9)
- Manejo de valores nulos
- Codificación one-hot encoding
- Normalización MinMaxScaler
- Balanceo con SMOTE

---

## Modelos y Técnicas

**Aprendizaje Supervisado:** SVM, Naive Bayes, Decision Tree, Random Forest

**Aprendizaje No Supervisado:** PCA, t-SNE, K-Means, DBSCAN

**Técnicas de Preprocesamiento:** One-Hot Encoding, MinMaxScaler, SMOTE

---

## Estructura del Proyecto

```
AFINIX/
│
├── Proyecto_IA/
│   ├── AFINIX.ipynb                              # Notebook principal
│   ├── match_model_tree_limitado.pkl             # Modelo Decision Tree
│   ├── match_model_tree_v2.pkl                   # Modelo Decision Tree v2
│   ├── random_forest_model.pkl                   # Modelo Random Forest
│   ├── Fase1-proyecto de inteligencia artificial (1).pdf
│   ├── Fase2-proyecto de inteligencia artificial.pdf
│   └── PRESENTACIÓN FINAL- AFINIX.pdf
│
├── banner (2).jpeg                           # Banner del proyecto
├── README.md                                 # Este archivo
└── .git/                                     # Control de versiones
```

---

## Resultados

### **Clasificación (Predicción de Match)**

El modelo **SVM** demostró el mejor desempeño con **73.12% de accuracy**, superando significativamente a los demás:

- **SVM**: 73.12% - Mejor balance entre precisión y recall
- **Naive Bayes**: 70.88% - Buen rendimiento probabilístico
- **Decision Tree**: 70.31% - Interpretabilidad clara
- **Random Forest**: 66.67% - Menor rendimiento

### **Clustering (Segmentación de Perfiles)**

Se identificaron **6 grupos principales** de usuarios con características similares:

- **K-Means**: Grupos bien definidos y balanceados
- **DBSCAN**: Detección de patrones densos y outliers
- **Visualizaciones**: 5 gráficas comparativas (PCA 2D + t-SNE)

### **Insights Principales:**

1. Los perfiles se agrupan principalmente por edad y orientación
2. Variables de estilo de vida (alimentación, bebidas) tienen alta relevancia
3. La reducción dimensional con PCA preserva >80% de varianza
4. t-SNE revela clusters no lineales más complejos

---

## Enlaces del Proyecto

<div align="center">

### **Recursos del Proyecto**

| Recurso | Enlace |
|---------|--------|
| **Código Fuente** | [Google Colab](https://colab.research.google.com/drive/1ASgdQfLB5zdqpfFrasf7p7D4SR-u8L0o#scrollTo=OFkDjsBNe8yR) |
| **Video Presentación** | [YouTube](https://youtu.be/l3lErUHyQB4?si=EdnQhM-URCJmPHT) |
| **Repositorio GitHub** | [GitHub](https://github.com/n4ncy27/AFINIX) |
| **Dataset** | [Kaggle](https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles) |
| **Diapostivas en canva** | [Canva](https://www.canva.com/design/DAG5dAEYWM8/UHCxQJcpJRL85pHLCUNEPw/edit) |

</div>

---

## Instalación y Uso

### **Nota Importante sobre el Dataset**

⚠️ **El dataset de OkCupid no se incluye en este repositorio** debido a sus grandes dimensiones (~60,000 registros). GitHub tiene limitaciones de tamaño para los archivos subidos. 

Para ejecutar el proyecto correctamente, **debes descargar el dataset** antes de trabajar con el notebook:

1. Dirígete a [Kaggle - OkCupid Profiles](https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles)
2. Descarga el archivo `okcupid_profiles.csv`
3. Coloca el archivo en una carpeta `data/` dentro del directorio del proyecto
4. Ahora podrás ejecutar el notebook sin problemas

### **Requisitos Previos**

```bash
Python 3.8+
pip
Google Colab (recomendado) o Jupyter Notebook
```

### **Instalación**

```bash
# Clonar el repositorio
git clone https://github.com/n4ncy27/AFINIX.git
cd AFINIX

# Instalar dependencias
pip install -r requirements.txt
```

### **Dependencias Principales**

```txt
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
imbalanced-learn>=0.8.0
```

### **Ejecución**

```bash
# Opción 1: Google Colab (Recomendado)
# 1. Subir el notebook a Google Drive
# 2. Abrir con Google Colab
# 3. Ejecutar todas las celdas

# Opción 2: Jupyter Local
jupyter notebook 01_exploratory_data_analysis.ipynb
```

---

## Visualizaciones

El proyecto incluye **5 visualizaciones principales**:

1. **PCA 2D** - Reducción dimensional sin clusters
2. **K-Means en PCA** - 6 clusters en espacio reducido
3. **DBSCAN en PCA** - Clustering basado en densidad
4. **K-Means con t-SNE** - Visualización no lineal
5. **DBSCAN con t-SNE** - Detección de outliers

---

## Contexto Académico

<div align="center">

<img src="logo.webp" width="200" alt="Logo UIS">

**Curso:** Inteligencia Artificial  
**Institución:** Universidad Industrial de Santander (UIS)  
**Semestre:** [Semestre Actual]  
**Año:** 2025

</div>

---

## Agradecimientos

- **OkCupid** por proporcionar el dataset para investigación académica
- **Kaggle Community** por el preprocesamiento y documentación
- **Scikit-learn** por las herramientas de Machine Learning
- Profesores y compañeros del curso de IA

---

<div align="center">

### Hecho con pasión por el equipo AFINIX

**¿Preguntas o sugerencias?** Abre un [Issue](https://github.com/n4ncy27/AFINIX/issues) o contáctanos directamente.

---

**Si este proyecto te fue útil, considera darle una estrella en GitHub**

