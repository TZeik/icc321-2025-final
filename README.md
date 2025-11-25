
---

# 📊 Proyecto Final: Inteligencia de Negocios y Minería de Datos

## 📘 Informe de Proyecto Final

**Materia:** Inteligencia de Negocios (ICC-321-T)
**Tema:** Dashboard Interactivo y Modelo de Minería de Datos Descriptivo

**Autores:**

* Randy Alexander Germosén Ureña *(1013-4707)*
* Fernando Almonte Delgado *(1015-7628)*

**Repositorio:**
[icc321-2025-final](https://github.com/TZeik/icc321-2025-final) <img src="https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg" width="15" height="15"/>

---

## 🎯 Objetivo del Proyecto

El propósito de este proyecto es desarrollar una solución integral de Inteligencia de Negocios utilizando datos públicos del gobierno de la República Dominicana. Consta de dos componentes principales:

1. **Dashboard Interactivo:** Permite visualizar y monitorear métricas de gasto y nómina para apoyar la toma de decisiones.
2. **Modelo de Minería de Datos:** Implementación de un modelo descriptivo (Clustering) para descubrir patrones y segmentar perfiles de empleados.

---

## 📂 Datasets Utilizados

Se procesaron y unificaron datos históricos abarcando el periodo **2018–2025**:

1. **Nómina de la Contraloría General de la República:**
   Información detallada sobre empleados, cargos, departamentos y sueldos.
2. **Índice de Precios al Consumidor (IPC):**
   Datos del Banco Central utilizados para calcular el **salario real** (ajustado por inflación) en comparación con el salario nominal.

---

## 🧠 Metodología

El desarrollo del proyecto se estructuró en las siguientes fases técnicas:

### 1. Ingeniería de Datos (ETL)

* **Extracción y Limpieza:**

  * Unificación de múltiples archivos CSV mensuales/anuales.
  * Estandarización de nombres de cargos, normalización de formatos monetarios y corrección de codificación (`latin-1`, `utf-8`).
  * Homogeneización de los nombres de los meses.
* **Enriquecimiento:**

  * Cruce entre nómina e IPC para calcular la pérdida de poder adquisitivo.

### 2. Almacenamiento (Data Warehousing)

* Implementación de un **Data Warehouse** local con **SQLite**.
* Diseño bajo un **Esquema en Estrella**, con:

  * Tabla de hechos: `fact_nomina`
  * Tablas de dimensiones: `dim_empleado`, `dim_tiempo`

### 3. Visualización (Dashboard)

* Creación de Dashboard interactivo en **Tableau Public**.
* Diseño de KPIs como:

  * Gasto total,
  * Brecha salarial,
  * Evolución de plantilla,
  * Tendencias del salario real vs nominal.

### 4. Minería de Datos (Machine Learning)

* **Preprocesamiento:**
  Codificación de variables categóricas y escalado numérico.
* **Modelado:**
  Aplicación de **K-Means Clustering** para identificar grupos de empleados con características similares.
* **Evaluación:**

  * Método del Codo
  * Coeficiente de Silueta

---

## 📊 Resultados Principales

La solución permite analizar hallazgos relevantes como:

* Diferencias entre **Sueldo Nominal** y **Sueldo Real** a lo largo del tiempo.
* Identificación de departamentos con mayor incremento en el gasto de nómina.
* Clusters de empleados basados en sueldo, cargo y antigüedad, revelando patrones ocultos en la organización.

---

## 🧩 Herramientas Utilizadas

### Lenguajes y Entorno

* **Python 3.x** (Jupyter Notebook)

### Librerías Principales

* `pandas` — Manipulación y limpieza de datos
* `sqlite3` — Data Warehouse local
* `scikit-learn` — Algoritmo K-Means y métricas
* `matplotlib` — Visualización del método del codo

### Visualización

* **Tableau Public** — Dashboard interactivo final

---

