# Análisis Exploratorio de Datos (EDA) con Python

## Descripción del Proyecto
Este proyecto tiene como objetivo realizar un **Análisis Exploratorio de Datos (EDA)** sobre campañas de marketing de una institución bancaria portuguesa. Las campañas se basaron en llamadas telefónicas y, en muchos casos, se requirieron múltiples contactos para determinar si el cliente suscribiría un depósito a plazo bancario.

## Objetivo
Aplicar técnicas de **transformación y limpieza de datos**, realizar un **análisis descriptivo**, visualizar los datos y elaborar un **informe explicativo** con hallazgos clave.

## Herramientas Utilizadas
- Python
- Pandas
- Matplotlib
- Seaborn
- Visual Studio Code
- Jupyter Notebook

## Requisitos del Proyecto
- Transformación y limpieza de los datos.
- Análisis descriptivo de los datos.
- Visualización de los datos.
- Informe explicativo del análisis.

---

## **1. Carga y Exploración de Datos**

### **1.1 Carga de los Datos**
Los datos provienen de:
- **`bank-additional.csv`**: Información sobre clientes y campañas de marketing.
- **`customer-details.xlsx`**: Datos demográficos de clientes en distintas hojas.

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Cargar datos de marketing
bank_df = pd.read_csv("data/bank-additional.csv", sep=";")

# Cargar datos de clientes (diferentes hojas del Excel)
customer_2012 = pd.read_excel("data/customer-details.xlsx", sheet_name='2012')
customer_2013 = pd.read_excel("data/customer-details.xlsx", sheet_name='2013')
customer_2014 = pd.read_excel("data/customer-details.xlsx", sheet_name='2014')
```

### **1.2 Unificación de Datos**
Antes de fusionar los datos:
- Se renombran las columnas de ID en `customer-details.xlsx`.
- Se combinan los datos de clientes en un solo DataFrame.

```python
# Renombrar la columna ID para que coincida en ambas tablas
customer_2012.rename(columns={'ID': 'id_'}, inplace=True)
customer_2013.rename(columns={'ID': 'id_'}, inplace=True)
customer_2014.rename(columns={'ID': 'id_'}, inplace=True)

# Concatenar datos de clientes en un solo DataFrame
customer_df = pd.concat([customer_2012, customer_2013, customer_2014], ignore_index=True)

# Fusionar con los datos de marketing usando la clave id_
merged_df = pd.merge(bank_df, customer_df, on='id_', how='left')
```

---

## **2. Transformación y Limpieza de Datos**

### **2.1 Identificación y Manejo de Valores Nulos**
```python
# Identificar valores nulos
print(merged_df.isnull().sum())

# Rellenar valores nulos en variables numéricas con la media
num_cols = merged_df.select_dtypes(include=['number']).columns
merged_df[num_cols] = merged_df[num_cols].fillna(merged_df[num_cols].mean())
```

### **2.2 Conversión de Tipos de Datos**
```python
# Convertir fechas a datetime
merged_df['date'] = pd.to_datetime(merged_df['date'], format='%d-%b-%Y', errors='coerce')
merged_df['Dt_Customer'] = pd.to_datetime(merged_df['Dt_Customer'], errors='coerce')

# Convertir variables categóricas
cat_cols = ['job', 'marital', 'education', 'default', 'housing', 'loan', 'contact', 'poutcome', 'y']
merged_df[cat_cols] = merged_df[cat_cols].astype('category')
```

### **2.3 Eliminación de Duplicados**
```python
# Eliminar duplicados
merged_df.drop_duplicates(inplace=True)
```

### **2.4 Creación de Nueva Variable**
```python
# Nueva columna: Total de hijos en el hogar
merged_df['Total_Children'] = merged_df['Kidhome'] + merged_df['Teenhome']
```

---

## **3. Análisis Descriptivo y Visualización**

### **3.1 Estadísticas Descriptivas**
```python
print(merged_df.describe())
```

### **3.2 Análisis de Correlación**
```python
# Calcular matriz de correlación y visualizarla
plt.figure(figsize=(12, 8))
sns.heatmap(merged_df.corr(), annot=True, cmap='coolwarm')
plt.title('Matriz de Correlación')
plt.show()
```

### **3.3 Distribución de la Duración de Llamadas**
```python
plt.figure(figsize=(10,5))
sns.histplot(merged_df['duration'], bins=50, kde=True)
plt.title('Distribución de la Duración de las Llamadas')
plt.xlabel('Duración (segundos)')
plt.ylabel('Frecuencia')
plt.show()
```

---

## **4. Informe Explicativo del Análisis**

- **Introducción**: Propósito del análisis y estructura de los datos.
- **Transformación y Limpieza**: Acciones realizadas para mejorar la calidad de los datos.
- **Análisis Descriptivo**: Estadísticas y patrones clave.
- **Visualización**: Representaciones gráficas de los hallazgos.
- **Conclusiones**: Insights obtenidos y posibles recomendaciones.

---

## **5. Organización del Proyecto**

```
📂 DatosProyecto/
│── 📁 data/ (Archivos CSV y Excel originales)
│── 📁 scripts/ (Código Python del EDA)
│── 📜 Python_for_data.ipynb (Notebook con el análisis)
│── 📜 README.md (Este documento explicativo)
```

Este README servirá como guía de referencia para cualquier persona que quiera entender y replicar el análisis. 🚀

