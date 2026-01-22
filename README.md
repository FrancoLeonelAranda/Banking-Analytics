# Banking Analytics – Exploratory Data Analysis (EDA)

## Descripción del Proyecto
Este proyecto consiste en un **Análisis Exploratorio de Datos (EDA)** aplicado a un conjunto de datos bancarios con información demográfica, financiera y de comportamiento de clientes.  
El objetivo es identificar **patrones relevantes**, **relaciones entre variables** y posibles **implicancias para análisis de riesgo crediticio y segmentación de clientes**.

El proyecto forma parte de un caso práctico de **Banking Analytics**, con una segunda etapa orientada a visualización y análisis en **Power BI**.

---

## Objetivos del Análisis
- Comprender la estructura y calidad del dataset
- Analizar la distribución de variables categóricas y numéricas
- Identificar relaciones bivariadas relevantes
- Detectar posibles problemas de **multicolinealidad**
- Extraer conclusiones útiles para futuras etapas de modelado o reporting

---

## Dataset
El dataset contiene información de **3000 clientes** e incluye variables como:

- Datos demográficos (edad, nacionalidad, ocupación)
- Productos financieros (préstamos, depósitos, tarjetas)
- Saldos en diferentes tipos de cuentas
- Variables categóricas de segmentación y riesgo

Los datos se obtienen desde una base **SQL Server**, consultada mediante `pyodbc`.

---

## 🧰 Tecnologías Utilizadas
- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SQL Server**
- **Git & GitHub**
- **Jupyter Notebook**

---

## 📁 Estructura del Repositorio
Banking-Analytics/
│
├── notebooks/
│ └── banking_case.ipynb
│
├── sql/
│ └── create_database.sql
│
└── README.md


## 🔍 Análisis Realizado

### 1️⃣ Análisis Descriptivo
- Estadísticas resumen de variables numéricas
- Verificación de tipos de datos
- Chequeo de valores faltantes

### 2️⃣ Feature Engineering
- Creación de la variable **Income Band** mediante cuantiles sobre `Estimated_Income`

### 3️⃣ Análisis Univariado
- Distribución de variables categóricas
- Histogramas de variables numéricas clave

### 4️⃣ Análisis Bivariado
- Comparación de variables categóricas por nacionalidad
- Exploración de relaciones entre variables financieras

### 5️⃣ Análisis de Correlación
- Matriz de correlación entre variables numéricas
- Identificación de relaciones fuertes entre saldos bancarios

---

## Principales Conclusiones del EDA
- Se observan **fuertes correlaciones** entre `Bank_Deposits`, `Checking_Accounts` y `Saving_Accounts`, lo que sugiere **redundancia y posible multicolinealidad**.
- El `Estimated_Income` presenta una relación **moderada a baja** con las variables de ahorro, indicando que el ingreso no explica por sí solo el comportamiento financiero.
- Existe una relación positiva entre distintos tipos de crédito, reflejando un **uso combinado de productos financieros**.
- El `Credit_Card_Balance` muestra correlaciones moderadas con la mayoría de las variables, evidenciando un uso transversal de la tarjeta de crédito.

Estos hallazgos sirven como base para etapas posteriores de **modelado**, **reducción de variables** y **visualización avanzada**.

---

## Próximos Pasos
- Desarrollo de dashboards en **Power BI**
- Segmentación de clientes
- Análisis orientado a **riesgo crediticio**
- Preparación de variables para modelos predictivos

---

## Autor
**Franco Aranda**  
Data Analytics | Banking & Risk  
