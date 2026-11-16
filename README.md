# Análisis Estadístico de la Calidad del Sueño

Este repositorio contiene el desarrollo de un proyecto académico para la asignatura de **Estadística Computacional**, perteneciente a la carrera de **Ingeniería Civil Informática** de la **Universidad Técnica Federico Santa María (UTFSM)**.

## Descripción General

El sueño es un pilar fundamental para la salud física, mental y el bienestar general. El objetivo principal de este proyecto es analizar cómo diversos factores del estilo de vida, hábitos diarios y condiciones fisiológicas influyen en la duración y calidad del descanso de las personas. A través de herramientas de estadística descriptiva e inferencial en Python, se buscan identificar patrones, distribuciones y relaciones significativas entre las variables estudiadas.

## Dataset y Variables

El estudio se basa en el conjunto de datos *Sleep Health and Lifestyle Dataset*, el cual recopila información sobre distintos perfiles demográficos, hábitos y métricas de salud:

- **Datos demográficos y laborales:** Género (`Gender`), Edad (`Age`), Ocupación (`Occupation`).
- **Métricas de sueño:** Duración del sueño en horas (`Sleep Duration`), Calidad del sueño en escala subjetiva (`Quality of Sleep`), Trastornos del sueño (`Sleep Disorder`: Ninguno, Insomnio, Apnea del sueño).
- **Estilo de vida y salud física:** Nivel de actividad física (`Physical Activity Level`), Nivel de estrés (`Stress Level`), Categoría de IMC (`BMI Category`), Presión arterial (`Blood Pressure`), Frecuencia cardíaca en reposo (`Heart Rate`) y Pasos diarios (`Daily Steps`).

## Contenido del Proyecto

El análisis se desarrolla íntegramente en el notebook [ProyectoEstaca.ipynb](file:///home/marto/Documentos/Proyectos/Calidad_de_sueno/ProyectoEstaca.ipynb) y abarca las siguientes etapas:

1. **Limpieza y Preprocesamiento de Datos:**
   - Tratamiento e imputación de valores nulos (específicamente en la variable de trastornos del sueño).
   - Estandarización de categorías (ej. `BMI Category`).
   - Detección y filtrado de valores atípicos (*outliers*) en variables cuantitativas utilizando el criterio del Rango Intercuartílico (`IQR`), generando un conjunto de datos limpio (`dataset_clean.csv`).

2. **Análisis Exploratorio de Datos (EDA):**
   - Visualización de distribuciones y frecuencias mediante gráficos de barras, histogramas, gráficos de cajas (*boxplots*) y diagramas de dispersión (*scatterplots*).
   - Exploración de relaciones entre variables clave, tales como actividad física, pasos diarios, nivel de estrés, IMC, ocupación, ritmo cardíaco y trastornos del sueño.

3. **Estimación de Parámetros y Ajuste de Distribuciones:**
   - Estimación de parámetros para variables continuas (`Heart Rate` y `Sleep Duration`) asumiendo una distribución Normal mediante el **Método de los Momentos** y el **Método de Máxima Verosimilitud (MLE)**.
   - Comparación gráfica entre la distribución empírica y las Funciones de Densidad de Probabilidad (FDP) teóricas.

4. **Inferencia Estadística e Intervalos de Confianza:**
   - Cálculo de intervalos de confianza y márgenes de error (incertidumbre).
   - Análisis del tamaño muestral y variación del nivel de significancia ($\alpha$) requeridos para reducir la incertidumbre en un porcentaje determinado.

5. **Pruebas de Bondad de Ajuste y Contrastes de Hipótesis:**
   - Aplicación de la prueba de **Kolmogorov-Smirnov (KS)** para evaluar el ajuste de las variables de estudio frente a distribuciones teóricas (Normal y Exponencial).
   - Pruebas de hipótesis para la comparación de varianzas (prueba $F$) y diferencia de medias entre grupos poblacionales (prueba $t$ de Welch para varianzas desconocidas y distintas, comparando el pulso cardíaco según ocupación).

6. **Modelamiento mediante Regresión Lineal:**
   - Implementación de un modelo de Regresión Lineal Simple mediante Mínimos Cuadrados Ordinarios (**OLS**) para explicar y cuantificar el impacto del nivel de estrés (`Stress Level`) sobre la calidad del sueño (`Quality of Sleep`).

## Tecnologías y Librerías Utilizadas

- **Lenguaje:** Python 3
- **Entorno:** Jupyter Notebook / Google Colab
- **Librerías principales:**
  - `pandas` y `numpy` (manipulación de datos y cálculo numérico)
  - `matplotlib` y `seaborn` (visualización de datos)
  - `scipy.stats` (distribuciones de probabilidad, intervalos de confianza y pruebas de hipótesis)
  - `statsmodels` (regresión lineal OLS)

## Autores

- **Axel Tapia**
- **Benjamín Cegarra**
- **Martín Espinoza**
- **Samira Estay**
