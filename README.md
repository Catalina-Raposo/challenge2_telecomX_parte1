# challenge2_telecomX_parte1

Aquí tienes un **README.md** claro y profesional para acompañar tu notebook `TelecomX_LATAM.ipynb`. Está pensado para un proyecto de análisis de datos o portafolio de ciencia de datos.

---

# 📊 TelecomX LATAM – Análisis de Evasión de Clientes (Churn)

## 📌 Descripción del Proyecto

Este proyecto analiza el **abandono de clientes (churn)** en la empresa ficticia **Telecom X LATAM**.
El objetivo principal es **identificar los factores que influyen en la cancelación del servicio**, utilizando técnicas de **análisis exploratorio de datos (EDA)** y transformación de datos.

El análisis se desarrolla a partir de un dataset en formato **JSON**, el cual contiene información sobre clientes, servicios contratados, características de la cuenta y comportamiento de facturación.

Este proyecto sigue un flujo típico de análisis de datos:

1. **Extracción de datos**
2. **Transformación y limpieza**
3. **Análisis exploratorio**
4. **Interpretación de resultados**

---

# 🎯 Objetivos

* Analizar la **tasa de evasión de clientes**.
* Identificar **variables que influyen en el churn**.
* Comprender el comportamiento de los clientes según:

  * Tipo de contrato
  * Servicios contratados
  * Antigüedad
  * Facturación
* Generar **insights útiles para la retención de clientes**.

---

# 📂 Estructura del Proyecto

```
TelecomX_LATAM/
│
├── TelecomX_LATAM.ipynb    # Notebook principal con todo el análisis
├── TelecomX_Data.json      # Dataset original en formato JSON
└── README.md               # Documentación del proyecto
```

---

# 🧩 Flujo del Análisis

## 1️⃣ Extracción de Datos

Se carga el dataset desde un archivo JSON y se convierte en un **DataFrame de pandas** para su manipulación.

```python
import pandas as pd
import json
```

---

## 2️⃣ Transformación de Datos

El dataset original contiene **estructuras anidadas**, por lo que se realiza un proceso de **normalización y desanidamiento**.

Se separan diferentes componentes:

* Información del cliente
* Servicios telefónicos
* Servicios de internet
* Información de la cuenta

Posteriormente se realiza:

* Limpieza de datos
* Conversión de variables
* Eliminación de valores inconsistentes
* Creación de variables derivadas

---

## 3️⃣ Análisis Exploratorio de Datos (EDA)

Se analizan variables **numéricas y categóricas** para entender qué factores se relacionan con la evasión.

### Estadísticas descriptivas

Se calculan métricas como:

* Promedio
* Desviación estándar
* Mínimo y máximo

para variables como:

* Antigüedad del cliente
* Cargos mensuales
* Cargos totales

---

### Análisis por Variables Categóricas

Se analiza cómo afecta al churn:

* Tipo de contrato
* Servicios contratados
* Facturación

Esto permite identificar **segmentos de clientes con mayor riesgo de abandono**.

---

### Análisis por Variables Numéricas

Se estudia la relación entre churn y:

* Antigüedad del cliente
* Cargos mensuales
* Cargos totales

Utilizando visualizaciones como:

* Boxplots
* Distribuciones

---

## 4️⃣ Análisis de Correlación

Se construye una matriz de correlación para analizar la relación entre variables numéricas y la evasión.

Para esto, la variable **Churn** se convierte en una variable binaria:

```
Yes → 1
No → 0
```

Esto permite analizar qué variables tienen **mayor relación con la probabilidad de cancelación**.

---

# 📈 Principales Insights

Entre los hallazgos más relevantes se observa que:

* Los **clientes con contratos mensuales** presentan mayor tasa de cancelación.
* Los clientes con **mayores cargos mensuales** tienden a cancelar con mayor frecuencia.
* La **antigüedad del cliente** está inversamente relacionada con el churn:
  clientes nuevos cancelan más que clientes antiguos.

Estos resultados sugieren oportunidades para mejorar estrategias de **retención de clientes**.

---

# 🛠️ Tecnologías Utilizadas

* **Python**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

---

# ▶️ Cómo Ejecutar el Proyecto

1. Clonar el repositorio o descargar los archivos.

```
git clone <repositorio>
```

2. Instalar dependencias necesarias:

```
pip install pandas matplotlib seaborn
```

3. Ejecutar el notebook:

```
jupyter notebook TelecomX_LATAM.ipynb
```

---

# 📌 Posibles Mejoras Futuras

* Implementar **modelos de machine learning** para predicción de churn:

  * Regresión logística
  * Árbol de decisión
  * Random Forest
* Crear **modelos de scoring de clientes en riesgo**.
* Construir un **dashboard interactivo** para monitorear churn.

---  
