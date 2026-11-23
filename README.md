# ConnectaTel-Analysis
Análisis ejecutivo para ConnectaTel
# Análisis Exploratorio y Segmentación de Clientes — ConnectaTel

## Objetivo del proyecto
Realizar un análisis exploratorio de datos (EDA) sobre una base consolidada de **4,000 usuarios** (`user_profile`) para evaluar la calidad de los datos, identificar patrones de uso (llamadas, mensajes y minutos de llamada) y edad, segmentar a los clientes y generar conclusiones accionables para la oferta de planes de **ConnectaTel**.

## Datasets utilizados
* **Datos consolidados (`user_profile`)**: base de `4,000` registros que integra información demográfica y de actividad de los usuarios (`user_id`, `age`, `city`, `reg_date`, `churn_date`, `cant_mensajes`, `cant_llamadas`, `cant_minutos_llamada`), junto con las variables derivadas `grupo_uso` y `grupo_edad`.
* **Calidad y valores nulos observados**: `0` filas duplicadas (`0.00%`) sobre los `4,000` registros, y valores nulos en `churn_date` (`3,534` filas, `88.35%`), `city` (`565` filas, `14.12%`) y `reg_date` (`40` filas, `1.00%`).

## Etapas del análisis realizadas
1. **Revisión de calidad de datos y limpieza**: verificación de duplicados, nulos y rangos numéricos (`min`, `50%`, `max`).
2. **Análisis exploratorio (EDA) y validación de outliers**: exploración de variables numéricas y retención de valores extremos altos (`0.75%` a `2.72%` del dataset) por corresponder a patrones reales de uso intensivo.
3. **Segmentación de clientes**:
   * `grupo_uso`: *Bajo uso*, *Uso medio* (`2,943` usuarios / `73.58%`[cite: 1]) y *Alto uso*.
   * `grupo_edad`: *Joven*, *Adulto* (`2,018` usuarios / `50.45%`[cite: 2]) y *Adulto Mayor*.
4. **Visualización de segmentos**: gráficos de barras (`seaborn` / `matplotlib`) para la distribución por nivel de uso y tramo etario[cite: 1, 2].
5. **Insight ejecutivo y recomendaciones**: síntesis de hallazgos clave y propuestas de planes orientadas a los distintos perfiles de uso y edad.

## Cómo ejecutar el notebook
* **En Google Colab**:
  1. Abre el archivo Data_analysis_2026 desde el repositorio en GitHub o cárgalo directamente en Google Colab.
  2. Ejecuta las celdas en orden de arriba hacia abajo (`Runtime` → `Run all` o `Entorno de ejecución` → `Ejecutar todas`).
* **En local (Jupyter Notebook / JupyterLab)**:
  1. Clona el repositorio y asegúrate de tener instaladas librerías como `pandas`, `numpy`, `matplotlib` y `seaborn`.
  2. Abre el *notebook* y ejecuta las celdas secuencialmente.

## Guía rápida de reproducción
1. Verifica que los datos o archivos de entrada estén accesibles en la ruta esperada por el *notebook*.
2. Corre las celdas de carga, inspección y creación de las variables `grupo_uso` y `grupo_edad`.
3. Revisa las tablas de frecuencia, los gráficos de segmentación y el resumen ejecutivo final.
