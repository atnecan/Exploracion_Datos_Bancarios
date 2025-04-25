# Proyecto de Análisis Exploratorio de Datos (EDA) con Python

Este proyecto tiene como objetivo analizar datos de campañas de marketing directo de una institución bancaria portuguesa. Se aplican técnicas de transformación y limpieza de datos, análisis descriptivo, visualización y se elabora un informe explicativo, todo ello utilizando Python.

## 1. Descripción del Proyecto

Las campañas de marketing se basaron en llamadas telefónicas a clientes. A menudo, se necesitará más de un contacto para determinar si el cliente suscribiría un depósito a plazo. En este repositorio, se documenta todo el proceso de Análisis Exploratorio de Datos (EDA), que incluye:

- Limpieza y transformación de datos.
- Análisis descriptivo (estadísticas, correlaciones, etc.).
- Visualización de resultados clave.
- Informe con hallazgos y conclusiones.

## 2. Objetivo Principal

Identificar los factores que influyen en la suscripción de productos bancarios, con el fin de optimizar futuras campañas de marketing basadas en datos.

## 3. Conjuntos de Datos Utilizados

- **bank-additional.csv**: 
  - Información sobre los contactos realizados a cada cliente: edad, ocupación, duración de la llamada, número de contactos, etc.
  - Incluye variables macroeconómicas (tasa de empleo, índice de precios, etc.).
  - Indica si el cliente suscribió finalmente el depósito (y = “sí” o “no”).

- **customer-details.xlsx**: 
  - Archivo Excel con 3 hojas que corresponden a diferentes años de ingreso de los clientes al banco.
  - Proporciona datos demográficos y de comportamiento de compra: ingresos anuales, número de hijos, fecha de alta, etc.
  - Ambos conjuntos de datos se relacionan mediante un identificador único (id_o ID).

## 4. Herramientas y Librerías

- **Python 3**
- **Pandas** (manipulación y limpieza de datos)
- **Matplotlib** y **Seaborn** (visualizaciones)
- **Jupyter Notebook** (opcional, para un flujo de trabajo interactivo)
- **Visual Studio Code** (para edición y ejecución de cuadernos o scripts)
- **GitHub** (versionado del proyecto)

## 5. Estructura del Repositorio
├── backup/                    # Carpeta opcional para copias de seguridad de los datos.
├── data/                      # Carpeta donde se almacenan los archivos de datos originales (CSV, Excel, etc.).
├── notebooks/                 # Carpeta que contiene los notebooks de Jupyter con el análisis paso a paso.
├── visualizations/            # Carpeta para guardar las gráficas o visualizaciones generadas durante el análisis.
├── DataProject_Proyecto EDA con Python.docx  # Documento con detalles y requisitos del proyecto.
└── README.md                  # Archivo de documentación principal (este archivo).


## 6. Pasos para Ejecutar el Proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/atnecan/DatosProyecto.git
   cd DatosProyecto

 2. Instala las dependencias (opcional, si deseas un entorno limpio):
   pip install -r requirements.txt

   Asegúrate de contar con pandas, matplotlib y seaborn. Si no tienes un requirements.txt, instala las librerías manualmente:

   pip install pandas matplotlib seaborn

   Abre el Notebook (o archivo .py, si lo tienes) en tu editor preferido:
   Ejecuta el análisis para:
   Cargar y limpiar los datos.
   Realizar el análisis descriptivo y las visualizaciones.
   Observar los hallazgos y conclusiones al final del proceso.   

## 7. Análisis Realizado

### Transformación y Limpieza

- Eliminación de duplicados y corrección de nombres de columnas.
- Conversión de tipos (fechas, categóricas, numéricas).
- Manejo de valores nulos mediante imputación o eliminación según convenga.

### Análisis Descriptivo

- Cálculo de estadísticas (medias, medianas, desviaciones estándar, correlaciones).
- Exploración de relaciones entre variables demográficas y macroeconómicas.

### Visualización

- Uso de Matplotlib y Seaborn para histogramas, boxplots, gráficos de dispersión y barras.
- Identificación de patrones y tendencias relevantes.

### Informe Explicativo

- Hallazgos principales, como la importancia de la duración de la llamada o el ingreso del cliente.
- Conclusiones y posibles recomendaciones para optimizar la campaña de marketing.

## 8. Conclusiones y Recomendaciones

### Conclusiones

- Factores como la edad, los ingresos, la duración de la llamada o el método de contacto pueden influir significativamente en la decisión de suscripción.
- El contexto macroeconómico (tasa de empleo, índice de precios, etc.) también puede impactar la disposición del cliente a adquirir el producto.

### Recomendaciones

- Focalizar campañas en segmentos de clientes con mayor probabilidad de respuesta.
- Ajustar la duración de las llamadas y el contenido para optimizar la tasa de éxito.

## 9. Futuras Extensiones

Aunque este proyecto cumple con los requisitos de un Análisis Exploratorio de Datos (EDA), a futuro se podría implementar:

- Modelos predictivos de Machine Learning para pronosticar la suscripción.
- Análisis de segmentación más detallado.
- Integración con otras fuentes de datos.

## 10. Contribuciones

Este repositorio se considera finalizado y no se aceptan contribuciones adicionales. Sin embargo, siéntete libre de hacer un fork y adaptar el código a tus propias necesidades.

## 11. Licencia

No se ha asignado una licencia específica. Si reutilizas este contenido, se agradece la mención al autor original.