# 🌸 Pipeline de Análisis y Visualización: Clasificación de Flores Iris

## 🎯 Objetivo del Proyecto

Este proyecto demuestra un *pipeline* completo de análisis de datos, desde la limpieza inicial de datos hasta la creación de un *dashboard* interactivo en Power BI. El objetivo analítico es explorar las diferencias morfológicas entre las tres especies de flores Iris y generar métricas clave que faciliten la clasificación visual.

---

## 🛠️ Stack Tecnológico

| Etapa | Herramientas | Propósito y Técnicas Destacadas |
| :--- | :--- | :--- |
| **ETL & Limpieza** | **Python (Pandas)** | Limpieza, estandarización de columnas (de inglés a español) y análisis exploratorio inicial. |
| **Feature Engineering** | **Python (Pandas)** | Creación de nuevas características para el análisis de proporciones. |
| **Visualización/BI** | **Power BI, DAX** | Modelado de datos, creación de medidas dinámicas (ej., `SUM`, `DISTINCTCOUNT`) y diseño del *dashboard* final. |

---

## ✨ Logros y Feature Engineering

### 1. Feature Engineering Clave
Se implementó la **Ingeniería de Características** para crear nuevas métricas con alto poder discriminatorio, esenciales para la clasificación:
* **`Suma_Petalo`**: Suma del ancho y longitud del pétalo.
* **`radio`**: Proporción entre la longitud del pétalo y la longitud del sépalo (`petalo_longitud / sepalo_longitud`).

### 2. Hallazgos Analíticos
* **Virginica vs. Setosa**: El **radio** (`petalo_longitud / sepalo_longitud`) demostró ser la métrica más efectiva para separar claramente la especie *setosa* de *virginica* y *versicolor*.
* **Métricas Dinámicas**: Las medidas DAX confirmaron que existe un **Total de 68 valores distintos** para la métrica `Suma_Petalo`, mostrando una distribución diversa dentro del *dataset*.

---

## 📊 Dashboard de Power BI (Entregable Final)

El resultado final es un *dashboard* interactivo que permite filtrar por especie y visualizar el rendimiento de las métricas clave.

Captura de pantalla del Dashboard de Power BI mostrando el análisis de las flores Iris (especies, totales y ratios).

### Métrica Clave Presentada
El panel se centra en mostrar los **Totales de Pétalos/Sépalos** y el **Promedio del radio** por especie, lo cual facilita la toma de decisiones basada en la morfología.

---

## 📁 Estructura del Repositorio

Para replicar el análisis:

| Carpeta | Contenido |
| :--- | :--- |
| `notebooks/` | Código fuente en Python (`Analisis_Iris.ipynb`) para limpieza y *Feature Engineering*. |
| `data/raw/` | Datos originales sin procesar (`iris_original.csv`). |
| `data/processed/` | Datos limpios (`datos_limpios_para_BI.csv`), listos para ser consumidos por Power BI. |
| `reports/` | Archivo de Power BI (`Dashboard_Iris.pbix`). |
