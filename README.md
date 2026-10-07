# Predicción de cancelación y segmentación de clientes en Model Fitness

Proyecto de análisis de datos y Machine Learning enfocado en identificar patrones asociados con la cancelación de membresías de una cadena de gimnasios, predecir el riesgo de abandono y segmentar a los clientes para apoyar el desarrollo de estrategias de retención.

## Objetivo

Analizar el comportamiento de los clientes de Model Fitness para:

- Identificar características asociadas con la cancelación de membresías.
- Desarrollar un modelo para predecir el riesgo de abandono.
- Comparar diferentes algoritmos de clasificación.
- Identificar segmentos de clientes mediante técnicas de clustering.
- Detectar grupos con mayor riesgo de cancelación.
- Proponer estrategias de retención basadas en los resultados del análisis.

## Herramientas utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook

## Técnicas aplicadas

- Análisis exploratorio de datos (EDA)
- Análisis de correlaciones
- Estandarización de variables
- Regresión Logística
- Random Forest
- Evaluación mediante Accuracy, Precision y Recall
- Clustering jerárquico
- Dendrogramas
- K-Means
- Segmentación de clientes

## Proceso de análisis

El proyecto se desarrolló en cinco etapas principales:

1. Importación, revisión y preparación de los datos.
2. Análisis exploratorio del comportamiento de los clientes y de las variables relacionadas con la cancelación.
3. Desarrollo y comparación de modelos de clasificación para predecir el abandono.
4. Segmentación de clientes mediante clustering jerárquico y K-Means.
5. Identificación de segmentos de riesgo y elaboración de recomendaciones de negocio orientadas a mejorar la retención.

## Modelos predictivos

Se entrenaron dos modelos de clasificación para predecir la cancelación de clientes:

| Modelo | Accuracy | Precision | Recall |
|---|---:|---:|---:|
| Regresión Logística | 0.924 | 0.890 | 0.797 |
| Random Forest | 0.910 | 0.849 | 0.782 |

La **Regresión Logística** presentó el mejor desempeño en las tres métricas evaluadas.

El Recall resulta especialmente relevante para el objetivo del proyecto, ya que representa la capacidad del modelo para identificar correctamente a los clientes que realmente presentan riesgo de cancelación.

## Segmentación de clientes

Después del análisis predictivo, se utilizaron técnicas de clustering para identificar diferentes perfiles de clientes.

Los datos fueron estandarizados y se utilizó clustering jerárquico mediante un dendrograma como análisis exploratorio de la estructura de los segmentos. Posteriormente, se aplicó K-Means con cinco clústeres.

Las tasas de cancelación obtenidas fueron:

| Clúster | Tasa de cancelación |
|---|---:|
| 0 | 58.77% |
| 1 | 28.59% |
| 4 | 10.51% |
| 3 | 4.23% |
| 2 | 1.39% |

El **clúster 0** presentó el mayor riesgo de cancelación. Este segmento se caracteriza por contratos más cortos, menor frecuencia de asistencia durante el mes actual y menor antigüedad como cliente.

En contraste, el **clúster 2** presentó la menor tasa de cancelación y se caracteriza por contratos de mayor duración, mayor frecuencia de asistencia y una relación más estable con el gimnasio.

## Principales resultados

- La Regresión Logística obtuvo el mejor desempeño predictivo, con un Accuracy de **92.4%**.
- Se identificaron segmentos de clientes con diferencias importantes en sus tasas de cancelación.
- El segmento de mayor riesgo presentó una tasa de cancelación aproximada del **58.77%**.
- El segmento más estable presentó una tasa de cancelación de aproximadamente **1.39%**.
- Los resultados muestran diferencias entre los segmentos en variables relacionadas con la duración del contrato, frecuencia de asistencia y antigüedad del cliente.

## Recomendaciones de negocio

1. **Identificar anticipadamente clientes con alto riesgo de cancelación.**  
   Utilizar las predicciones del modelo para dirigir acciones de retención hacia clientes con mayor probabilidad de abandono.

2. **Promover contratos de mayor duración.**  
   Diseñar incentivos que faciliten la transición de membresías mensuales hacia contratos semestrales o anuales.

3. **Fomentar una mayor frecuencia de asistencia.**  
   Implementar recordatorios, retos, actividades grupales y beneficios por participación para aumentar la interacción de los clientes con el gimnasio.

4. **Aplicar estrategias diferenciadas por segmento.**  
   Utilizar los perfiles obtenidos mediante clustering para adaptar campañas y acciones de retención a las características de cada grupo.

## Conclusión

La combinación de modelos predictivos y técnicas de segmentación permitió identificar tanto clientes con mayor riesgo de cancelación como perfiles de comportamiento asociados con diferentes niveles de retención.

Los resultados pueden utilizarse como base para desarrollar una estrategia de retención más proactiva y focalizada, priorizando los segmentos con mayor riesgo y fomentando comportamientos asociados con una mayor permanencia.

## Archivos

- `proyecto_sprint_14.ipynb`: notebook principal con el análisis completo.
- `gym_churn_us.csv`: dataset utilizado para el análisis.
- `requirements.txt`: dependencias de Python necesarias para ejecutar el proyecto.

## Instalación de dependencias

Para instalar las librerías necesarias:

```bash
pip install -r requirements.txt