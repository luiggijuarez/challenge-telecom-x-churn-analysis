<h1>📊 Telecom X: Análisis de Evasión de Clientes (Churn Analysis)<h1>
  
<h2>🎯 Propósito del Proyecto<h2>
  
Este proyecto tiene como objetivo resolver el alto índice de evasión de clientes en Telecom X. A través de un proceso de ETL (Extract, Transform, Load), he transformado datos crudos provenientes de una API en un dataset refinado para identificar patrones de comportamiento que preceden a la cancelación del servicio.

El fin último es proporcionar al equipo de Ciencia de Datos una base sólida para construir modelos predictivos de retención.

<h2>📂 Estructura del Proyecto<h2>
  
La organización de los archivos sigue las buenas prácticas de Ciencia de Datos:

- TelecomX_LATAM.ipynb: Notebook principal con el flujo completo de Python.

- TelecomX_Data.json: Dataset original con estructuras anidadas (Simulación de API).

- TelecomX_Limpio_Analisis.csv: Dataset final después de la limpieza y transformación.

- TelecomX_diccionario.md: Documentación de las variables y reglas de negocio.

<h2>🛠️ Proceso de Ingeniería de Datos<h2>
  
**1. Extracción y Normalización**

Se utilizó pd.json_normalize para aplanar la estructura jerárquica del JSON, permitiendo el acceso a variables críticas como cargos y métodos de pago.

**2. Transformación (Data Wrangling)**

- **Limpieza de Tipos:** Conversión de la columna TotalCharges de texto a numérico.

- **Tratamiento de Nulos:** Se identificaron registros vacíos en clientes nuevos (tenure = 0), los cuales fueron normalizados a 0.0 para mantener la integridad del dataset.

- **Codificación Binaria:** Transformación de la variable objetivo Churn (Yes/No) a formato numérico (1/0) para análisis estadístico.

<h2>📈 Insights y Visualizaciones<h2>
Durante el Análisis Exploratorio de Datos (EDA), se obtuvieron los siguientes hallazgos clave:

- **⚠️ Riesgo por Contrato:** Los clientes con contratos "Month-to-month" tienen una probabilidad de evasión significativamente mayor.

- **📡 Desempeño de Fibra Óptica:** A pesar de ser un servicio premium, los usuarios de fibra presentan mayor deserción que los de DSL, sugiriendo problemas de precio o estabilidad.

- **💳 Métodos de Pago:** El uso de Electronic Check está fuertemente correlacionado con la evasión temprana.

<h2>🚀 Instrucciones de Ejecución<h2>
  
Para replicar este análisis en tu entorno local o en la nube:

1. Clonar el repositorio:

Bash
git clone https://github.com/tu-usuario/challenge-telecom-x-churn-analysis.git

2. Cargar en Google Colab:

- Sube el archivo .ipynb a Google Colab.
- Monta tu Google Drive para acceder al archivo JSON o súbelo directamente a la sesión.

3. Instalar dependencias:

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
Ejecutar celdas: Sigue el orden secuencial del notebook para completar el proceso de ETL.
