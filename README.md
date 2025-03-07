# Análisis Exploratorio de Datos (EDA) con Python

## Descripción del Proyecto
Este proyecto tiene como objetivo realizar un análisis exploratorio de los datos relacionados con campañas de marketing directo de una institución bancaria portuguesa. Las campañas de marketing se basaron en llamadas telefónicas, y a menudo se requerió más de un contacto con el mismo cliente para determinar si el producto (depósito a plazo bancario) sería suscrito o no.

## Objetivo
El objetivo del proyecto es aplicar técnicas de transformación y limpieza de datos, realizar un análisis descriptivo, visualizar los datos y elaborar un informe explicativo del análisis realizado.

## Herramientas Utilizadas
- Python
- Pandas
- Matplotlib
- Seaborn
- Visual Studio Code
- GitHub para el versionado del código

## Requisitos del Proyecto
- Transformación y limpieza de los datos.
- Análisis descriptivo de los datos.
- Visualización de los datos.
- Informe explicativo del análisis.

## Estructura del Proyecto
El proyecto está organizado en los siguientes apartados:

### 1. Carga de los Datos y Preparación
1.1 **Carga de Datos**
   - Se cargan los datos desde archivos CSV y Excel.
   - Se corrigen posibles errores en los nombres de las columnas.
   - Se crean copias de seguridad antes de modificar los datos.

1.2 **Unificación de Datos**
   - Se combinan los datos de clientes de diferentes años en un único DataFrame.
   - Se asegura que la clave de unión ('id_') esté correctamente definida antes de fusionar.

### 2. Transformación y Limpieza
2.1 **Identificación y Manejo de Valores Nulos**
   - Se identifican y rellenan valores nulos en columnas numéricas con la media.
   - Se convierten las columnas de fechas en formato datetime.

2.2 **Conversión de Tipos de Datos**
   - Se convierten variables categóricas para mejorar la eficiencia del análisis.
   - Se eliminan duplicados si los hay.

### 3. Análisis Descriptivo y Visualización
3.1 **Estadísticas Descriptivas**
   - Se calculan medias, medianas, desviaciones y distribuciones de las variables más relevantes.
   
3.2 **Análisis de Relaciones**
   - Se examinan correlaciones entre variables.
   - Se visualizan patrones con histogramas y boxplots.

3.3 **Visualizaciones Clave**
   - **Distribución de Edad de los Clientes**
   - **Duración de las Llamadas y su Influencia en la Suscripción**
   - **Relación entre Nivel Educativo y Probabilidad de Suscripción**
   - **Método de Contacto y Éxito de la Campaña**
   - **Ingresos y su Relación con la Suscripción**
   - **Influencia de la Tasa de Empleo y el Índice de Precios en la Decisión de los Clientes**

### 4. Informe Explicativo del Análisis
Se elabora un informe que incluye:
- Introducción y contexto del problema.
- Transformaciones y limpieza realizadas.
- Visualizaciones clave y hallazgos.
- Conclusiones y recomendaciones basadas en los datos analizados.

### 5. Instrucciones para Ejecutar el Proyecto
#### 5.1 Requisitos Previos
- Tener instalado Python y las librerías necesarias (`pandas`, `matplotlib`, `seaborn`).
- Clonar el repositorio desde GitHub:
  ```bash
  git clone <URL_DEL_REPOSITORIO>
  ```

#### 5.2 Ejecución
1. Abre el archivo del script en Visual Studio Code.
2. Ejecuta cada celda de código paso a paso en un entorno Jupyter Notebook o terminal.
3. Analiza los resultados obtenidos y visualiza los gráficos generados.

## Contribuciones
Si deseas contribuir a mejorar este análisis, puedes realizar un fork del repositorio y enviar tus propuestas a través de un pull request en GitHub.

---

📌 **Este README será actualizado conforme se agreguen mejoras al análisis.**

