<<<<<<< HEAD
# AFINIX - Sistema Inteligente de Compatibilidad con Machine Learning

<div align="center">

![Banner del Proyecto](https://via.placeholder.com/800x300/1E3A8A/FFFFFF?text=AFINIX+-+An%C3%A1lisis+de+Compatibilidad+con+IA)

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Sistema avanzado de predicción de compatibilidad basado en Machine Learning**

[Objetivo](#objetivo) • [Dataset](#dataset) • [Modelos](#modelos) • [Enlaces](#enlaces) • [Equipo](#autores)

</div>

---

<div align="center">

<img src="./assets/compatibility-icon.png" width="120" alt="Compatibilidad IA">

### *"La compatibilidad es la chispa que convierte el encuentro en destino"*

</div>

---

## Tabla de Contenido

- [Autores](#autores)
- [Objetivo](#objetivo)
- [Dataset](#dataset)
- [Modelos y Técnicas](#modelos)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Resultados](#resultados)
- [Enlaces del Proyecto](#enlaces)
- [Instalación y Uso](#instalación-y-uso)
- [Licencia](#licencia)

---

## Autores

<div align="center">

| Nombre | Código |
|--------|--------|
| **Johan Santiago Rojas Naranjo** | 2225005 |
| **Leyson David Celis Acelas** | 2225002 |
| **Nancy Liliana Saenz Moreno** | 2224510 |

</div>

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

### **Aprendizaje Supervisado** (Clasificación Binaria)

| Modelo | Accuracy | Descripción |
|--------|----------|-------------|
| **SVM (Support Vector Machine)** | 73.12% | Mejor rendimiento |
| **Naive Bayes** | 70.88% | Clasificador probabilístico |
| **Decision Tree** | 70.31% | Árbol de decisión |
| **Random Forest** | 66.67% | Ensamble de árboles |

### **Aprendizaje No Supervisado** (Clustering)

#### Reducción Dimensional:
- **PCA** (Principal Component Analysis)
  - 50 componentes para análisis
  - 2 componentes para visualización
  
- **t-SNE** (t-Distributed Stochastic Neighbor Embedding)
  - Perplexity: 50
  - Iteraciones: 1,000
  - Muestra: 10,000 perfiles

#### Algoritmos de Clustering:
- **K-Means**
  - 6 clusters
  - 30 inicializaciones
  
- **DBSCAN** (Density-Based Spatial Clustering)
  - eps: 2.8
  - min_samples: 10

### **Tecnologías Utilizadas:**

```
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
PCA, t-SNE, K-Means, DBSCAN, SVM, Naive Bayes, Decision Trees, Random Forest
```

---

## Estructura del Proyecto

```
AFINIX/
│
├── 01_exploratory_data_analysis.ipynb  # Notebook principal
│   ├── Análisis Exploratorio de Datos (EDA)
│   ├── Preprocesamiento y Limpieza
│   ├── Modelos Supervisados (Clasificación)
│   ├── Modelos No Supervisados (Clustering)
│   └── Visualizaciones y Resultados
│
├── data/
│   └── okcupid_profiles.csv              # Dataset original
│
├── results/
│   ├── okcupid_ENTREGA_FINAL_COMPLETA.csv  # Resultados con clusters
│   └── visualizations/                    # Gráficas generadas
│
├── README.md                          # Este archivo
└── requirements.txt                   # Dependencias
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

## Enlaces del Proyecto {#enlaces}

<div align="center">

### **Recursos del Proyecto**

| Recurso | Enlace |
|---------|--------|
| **Código Fuente** | [Google Colab](https://colab.research.google.com/drive/TU_ENLACE_AQUI) |
| **Video Presentación** | [YouTube](https://youtube.com/TU_VIDEO_AQUI) |
| **Repositorio GitHub** | [GitHub](https://github.com/TU_USUARIO/afinix-ml) |
| **Dataset** | [Kaggle](https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles) |
| **Documentación** | [GitHub Wiki](https://github.com/TU_USUARIO/afinix-ml/wiki) |

</div>

---

## Instalación y Uso

### **Requisitos Previos**

```bash
Python 3.8+
pip
Google Colab (recomendado) o Jupyter Notebook
```

### **Instalación**

```bash
# Clonar el repositorio
git clone https://github.com/TU_USUARIO/afinix-ml.git
cd afinix-ml

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

<img src="data:image/webp;base64,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" width="150" alt="Logo UIS">

**Curso:** Inteligencia Artificial  
**Institución:** Universidad Industrial de Santander (UIS)  
**Semestre:** [Semestre Actual]  
**Año:** 2025

</div>

---

## Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

## Agradecimientos

- **OkCupid** por proporcionar el dataset para investigación académica
- **Kaggle Community** por el preprocesamiento y documentación
- **Scikit-learn** por las herramientas de Machine Learning
- Profesores y compañeros del curso de IA

---

<div align="center">

### Hecho con pasión por el equipo AFINIX

**¿Preguntas o sugerencias?** Abre un [Issue](https://github.com/TU_USUARIO/afinix-ml/issues) o contáctanos directamente.

---

**Si este proyecto te fue útil, considera darle una estrella en GitHub**

</div>
=======
# AFINIX - Sistema Inteligente de Compatibilidad con Machine Learning

![Banner del Proyecto]("C:\Users\usuario\Downloads\Banner.jpeg")

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Sistema avanzado de predicción de compatibilidad basado en Machine Learning**

[Objetivo](#objetivo) • [Dataset](#dataset) • [Modelos](#modelos) • [Enlaces](#enlaces) • [Equipo](#autores)

</div>

---

<div align="center">

<img src="./assets/compatibility-icon.png" width="120" alt="Compatibilidad IA">

### *"La compatibilidad es la chispa que convierte el encuentro en destino"*

</div>

---

## Tabla de Contenido

- [Autores](#autores)
- [Objetivo](#objetivo)
- [Dataset](#dataset)
- [Modelos y Técnicas](#modelos)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Resultados](#resultados)
- [Enlaces del Proyecto](#enlaces)
- [Instalación y Uso](#instalación-y-uso)
- [Licencia](#licencia)

---

## Autores

<div align="center">

| Nombre | Código |
|--------|--------|
| **Johan Santiago Rojas Naranjo** | 2225005 |
| **Leyson David Celis Acelas** | 2225002 |
| **Nancy Liliana Saenz Moreno** | 2224510 |

</div>

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

### **Aprendizaje Supervisado** (Clasificación Binaria)

| Modelo | Accuracy | Descripción |
|--------|----------|-------------|
| **SVM (Support Vector Machine)** | 73.12% | Mejor rendimiento |
| **Naive Bayes** | 70.88% | Clasificador probabilístico |
| **Decision Tree** | 70.31% | Árbol de decisión |
| **Random Forest** | 66.67% | Ensamble de árboles |

### **Aprendizaje No Supervisado** (Clustering)

#### Reducción Dimensional:
- **PCA** (Principal Component Analysis)
  - 50 componentes para análisis
  - 2 componentes para visualización
  
- **t-SNE** (t-Distributed Stochastic Neighbor Embedding)
  - Perplexity: 50
  - Iteraciones: 1,000
  - Muestra: 10,000 perfiles

#### Algoritmos de Clustering:
- **K-Means**
  - 6 clusters
  - 30 inicializaciones
  
- **DBSCAN** (Density-Based Spatial Clustering)
  - eps: 2.8
  - min_samples: 10

### **Tecnologías Utilizadas:**

```
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
PCA, t-SNE, K-Means, DBSCAN, SVM, Naive Bayes, Decision Trees, Random Forest
```

---

## Estructura del Proyecto

```
AFINIX/
│
├── 01_exploratory_data_analysis.ipynb  # Notebook principal
│   ├── Análisis Exploratorio de Datos (EDA)
│   ├── Preprocesamiento y Limpieza
│   ├── Modelos Supervisados (Clasificación)
│   ├── Modelos No Supervisados (Clustering)
│   └── Visualizaciones y Resultados
│
├── data/
│   └── okcupid_profiles.csv              # Dataset original
│
├── results/
│   ├── okcupid_ENTREGA_FINAL_COMPLETA.csv  # Resultados con clusters
│   └── visualizations/                    # Gráficas generadas
│
├── README.md                          # Este archivo
└── requirements.txt                   # Dependencias
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

## Enlaces del Proyecto {#enlaces}

<div align="center">

### **Recursos del Proyecto**

| Recurso | Enlace |
|---------|--------|
| **Código Fuente** | [Google Colab](https://colab.research.google.com/drive/TU_ENLACE_AQUI) |
| **Video Presentación** | [YouTube](https://youtube.com/TU_VIDEO_AQUI) |
| **Repositorio GitHub** | [GitHub](https://github.com/TU_USUARIO/afinix-ml) |
| **Dataset** | [Kaggle](https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles) |
| **Documentación** | [GitHub Wiki](https://github.com/TU_USUARIO/afinix-ml/wiki) |

</div>

---

## Instalación y Uso

### **Requisitos Previos**

```bash
Python 3.8+
pip
Google Colab (recomendado) o Jupyter Notebook
```

### **Instalación**

```bash
# Clonar el repositorio
git clone https://github.com/TU_USUARIO/afinix-ml.git
cd afinix-ml

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

<img src="<img width="309" height="152" alt="image" src="https://github.com/user-attachments/assets/315e17f4-e7ec-4163-9709-9b3fb25bf426" />" alt="Logo UIS">


**Curso:** Inteligencia Artificial  
**Institución:** Universidad Industrial de Santander (UIS)  
**Semestre:** [Semestre Actual]  
**Año:** 2025

</div>

---

## Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

## Agradecimientos

- **OkCupid** por proporcionar el dataset para investigación académica
- **Kaggle Community** por el preprocesamiento y documentación
- **Scikit-learn** por las herramientas de Machine Learning
- Profesores y compañeros del curso de IA

---

<div align="center">

### Hecho con pasión por el equipo AFINIX

**¿Preguntas o sugerencias?** Abre un [Issue](https://github.com/TU_USUARIO/afinix-ml/issues) o contáctanos directamente.

---

**Si este proyecto te fue útil, considera darle una estrella en GitHub**

</div>




>>>>>>> 7467b1a5e5fac43b06ffaf26496ecee34dd86231
