# 📊 Análisis Exploratorio de Datos (EDA) - COVID-19

Este repositorio contiene un Análisis Exploratorio de Datos (EDA) sobre la pandemia de COVID-19, realizado en un Notebook de Jupyter (`EdaCovid19.ipynb`). El objetivo de este análisis es procesar, limpiar y visualizar múltiples fuentes de datos para entender la propagación, las tendencias y las características demográficas del virus en sus etapas iniciales.

## 📂 Fuentes de Datos

Este análisis integra y procesa tres conjuntos de datos diferentes. **Nota: Para ejecutar el notebook, necesitarás tener los siguientes archivos CSV en la misma carpeta:**

1.  `covid_19_data.csv`: Datos de series temporales con casos confirmados, muertes y recuperados por país/región.
2.  `COVID19_line_list_data.csv`: Datos a nivel de paciente (lista de casos) que incluyen información demográfica y de síntomas.
3.  `COVID19_open_line_list.csv`: Otra lista de casos detallada con datos demográficos y de resultados (ej. alta, fallecimiento).

## 📈 Análisis Realizado

El notebook está estructurado en varias secciones clave de análisis:

### 1. Limpieza y Preprocesamiento de Datos
* Renombrado de columnas para consistencia (ej. `ObservationDate` -> `Date`).
* Conversión de fechas a objetos `datetime`.
* Manejo de valores nulos (`NaN`) y eliminación de columnas irrelevantes.
* Creación de nuevas métricas, como `Active` (casos activos), `Mortality Rate` (tasa de mortalidad) y `Recovery Rate` (tasa de recuperación).

### 2. Análisis Global (Serie Temporal)
* Visualización de la evolución mundial de casos **Confirmados**, **Muertes** y **Recuperados** a lo largo del tiempo.
* Gráficos de la evolución de **casos activos** a nivel global.
* Análisis de las tasas de mortalidad y recuperación (en % por cada 100 casos) a lo largo del tiempo.

### 3. Análisis por País
* Rankings (Top 20) de países con más casos **Confirmados**, **Muertes** y **Casos Activos** mediante gráficos de barras interactivos.
* Rankings (Top 20) de países con las **tasas de mortalidad** y **tasas de recuperación** más altas y más bajas.
* Creación de un **mapa interactivo (Choropleth)** con `Folium` para visualizar la distribución geográfica de los casos confirmados en el mundo.

### 4. Análisis Demográfico (Line List Data)
* Análisis de la distribución de casos por **género** (hombre/mujer).
* Análisis de la distribución de casos por **edad** (histogramas y gráficos de violín).
* Visualización de los **síntomas** más comunes reportados (Top 10).
* Análisis cruzado de **resultados** (ej. "fallecido", "dado de alta") en relación con la edad y el género.

## 🛠️ Librerías Utilizadas

Este análisis utiliza las principales librerías del ecosistema de Data Science en Python:

* **Pandas:** Para la manipulación y limpieza de datos.
* **NumPy:** Para operaciones numéricas.
* **Matplotlib:** Para la creación de gráficos estáticos básicos.
* **Seaborn:** Para visualizaciones estadísticas avanzadas (distribuciones, violin plots, count plots).
* **Plotly Express:** Para la creación de gráficos interactivos (líneas, barras).
* **Folium:** Para la generación de mapas interactivos.
