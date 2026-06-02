# Motor Predictivo de Retención de Clientes (Churn) a Escala Big Data

##  Visión General
Este proyecto desarrolla una arquitectura de datos *End-to-End* diseñada para predecir y mitigar la cancelación de contratos (Churn) en el sector de telecomunicaciones. Utilizando procesamiento distribuido, el modelo identifica a los clientes en riesgo de fuga, traduciendo métricas matemáticas en impacto financiero directo.

##  Impacto de Negocio (ROI)
* **Capital Protegido Estimado:** **$6,814,250 USD** en costos de adquisición mitigados.
* **Aciertos Críticos:** Detección temprana de más de 27,000 clientes en riesgo.
* **Top 3 Factores de Riesgo Identificados:** Fricción en contratos mensuales, debilidad en la retención temprana (primeros meses) y sensibilidad al modelo de precios.

##  Stack Tecnológico y Arquitectura
* **Procesamiento Distribuido:** Apache Spark (PySpark) operando en un clúster local.
* **Ingeniería de Datos:** Técnicas de *Data Augmentation* para escalar la base fundacional a **+900,000 registros transaccionales**, validando la tolerancia de la arquitectura.
* **Machine Learning & MLOps:** Construcción de un *Pipeline* de vectorización automatizada y entrenamiento de un algoritmo **Gradient-Boosted Trees (GBTClassifier)**.
* **Evaluación:** ROC-AUC (87.88%) y visualización de datos ejecutiva (Matplotlib/Seaborn).

##  Cómo ejecutar este proyecto
El código completo está contenido en el notebook principal. Las dependencias requieren un entorno configurado con Java 11 y Apache Spark 4.0+.

## 📊 Business Intelligence & Visualización (Power BI)

Para traducir los hallazgos técnicos en decisiones ejecutivas, desarrollé un panel de control interactivo enfocado en el impacto financiero del *Churn*.

**Arquitectura del Modelo de Datos:**
*   **ETL & Limpieza:** Utilización de Power Query y lenguaje M para depurar tipos de datos automáticos erróneos y unificar la configuración regional contable.
*   **Modelo Relacional:** Construcción de un esquema de estrella (Star Schema) separando las dimensiones (`Dim_Contratos`) de la tabla de hechos (`Fast_Telco`).
*   **Motor DAX:** Creación de medidas escalables usando funciones como `CALCULATE` y `DIVIDE` para establecer KPIs seguros frente a errores.

**Insights Clave del Tablero:**
*   **Identificación del Riesgo:** El 42.7% del riesgo de abandono se concentra en contratos mensuales.
*   **Fuga de Capital:** Rastreo preciso de la pérdida de ingresos mensuales recurrentes (MRR), detectando que la mayor fuga financiera proviene de pagos mediante cheque electrónico.

> **Demostración de Interactividad:** 
> *El filtrado cruzado permite aislar el impacto financiero con un solo clic.*
> 
> <img width="1920" height="1080" alt="2026-06-02-02-18-23" src="https://github.com/user-attachments/assets/d5b39d70-63b1-4fc4-a6ea-204ebe7c1acc" />
