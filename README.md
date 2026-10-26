# Segmentación de inmuebles en arriendo – Machine Learning No Supervisado

**Universidad de Cundinamarca · Especialización en Inteligencia Artificial**
CADI – Introducción a Machine Learning (2026-2) · Docente: Ing. Wilson Rojas Reales, PhD(c)
**Estudiante:** Laura Fernanda López Mayorga

Aplicación de K-Means, clustering jerárquico (Ward), PCA y SVD para descubrir segmentos comerciales en un portafolio de 1.000 inmuebles en arriendo (Chapinero, Suba y Usaquén).

## Contenido

| Archivo | Descripción |
|---|---|
| `01_KMeans_Segmentacion_Inmuebles.ipynb` | Adaptación de `KMeansSegInmuebles.py`: carga del Excel, calidad de datos, EDA, codo/silueta, K-Means con k = 2, 3 y 4, escenario refinado y exportación de resultados. |
| `02_PCA_SVD_Jerarquico_Inmuebles.ipynb` | Adaptación de `Algoritmo_InmueblesPCA.py`: varianza explicada, cargas, visualización PC1-PC2, K-Means sobre componentes (ARI), SVD y clustering jerárquico. |
| `DATASET_INmuebles.xlsx` | Dataset entregado por el docente. |
| `inmuebles_segmentados.csv` | Id de cada inmueble con su clúster (k = 2, 3, 4) y segmento final. |
| `figuras/` | Gráficas generadas por los notebooks. |


## Resultados principales

- PCA: PC1 + PC2 explican el **66,26 %** de la varianza; PC1 (51,15 %) es un eje de “tamaño y valor” (precio, área, habitaciones, estrato).
- K-Means con las 9 variables: k = 2 tiene la mejor silueta (0,380); con k = 3 el grupo de acceso se divide por número de baños.
- K-Means k = 3 sobre las variables núcleo (silueta 0,482): **Económico** (419, $1,47 M), **Intermedio** (209, $3,13 M), **Premium** (372, $6,35 M).
- Clustering jerárquico de Ward ≈ K-Means (ARI = 0,997).
