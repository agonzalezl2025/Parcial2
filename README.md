# Parcial2

# Análisis del PIB Global con Python

# 📌 Descripción del Proyecto

En un mundo cada vez más interconectado, comprender el panorama económico global es esencial para formuladores de políticas, investigadores y empresas. Este proyecto permite aplicar los conceptos aprendidos en los laboratorios de Python mediante el análisis del World GDP Dataset, extraído del World Bank Group.

El dataset incluye información sobre el Producto Interno Bruto (PIB) de múltiples países desde 1960 hasta 2022, proporcionando una base sólida para examinar tendencias económicas, comparar desempeños nacionales y explorar correlaciones con otros indicadores económicos y sociales.

# 🎯 Objetivos

📊 Aplicar herramientas de análisis de datos en Python para estudiar la evolución del PIB global.

🔍 Explorar patrones económicos y tendencias a lo largo del tiempo.

🌍 Identificar diferencias en el crecimiento económico entre países y regiones.

📈 Visualizar datos de manera efectiva para comunicar hallazgos clave.

# 📂 Contenido del Proyecto

Exploración de Datos: Carga y limpieza del dataset para eliminar valores nulos o inconsistentes.

Análisis Descriptivo: Cálculo de estadísticas básicas sobre el crecimiento del PIB en diferentes países.

Visualización de Datos: Uso de librerías como Matplotlib y Seaborn para representar tendencias económicas.

Comparación Regional: Evaluación del crecimiento del PIB en distintas regiones geográficas.

Predicción de Tendencias: Aplicación de modelos de regresión para prever la evolución futura del PIB.


# Diccionario
| **Variable**      | **Tipo**             | **Descripción**                                                                                 |
|-------------------|----------------------|-------------------------------------------------------------------------------------------------|
| `country_name`    | String              | Nombre oficial del país.                                                                        |
| `country_code`    | String              | Código (generalmente ISO) que identifica al país (ej: “AFG”, “ALB”).                             |
| `year`            | Entero              | Año calendario correspondiente al valor del PIB.                                                |
| `value`           | Numérico (float)    | Valor del PIB. Verificar la unidad (millones, miles de millones, etc.).                         |
| `region`          | String              | Región geográfica del país (ej: “Latin America & Caribbean”, “East Asia & Pacific”).             |
| `income_group`    | String              | Clasificación del país según nivel de ingreso (ej: “Low income”, “High income”).                |


## :star2: Bono: Nueva Variable de PIB per Cápita

## Diccionario de Variables

| Columna           | Tipo   | Descripción                                                                                           |
|-------------------|--------|-------------------------------------------------------------------------------------------------------|
| `Country Code`    | String | Código o nombre del país (por ejemplo, `"AFG"`, `"Colombia"`, etc.)                                   |
| `Year`            | Int    | Año de la observación                                                                                 |
| `GDP`             | Float  | Producto Interno Bruto (PIB) total del país (en dólares)                                              |
| `GDP_per_capita`  | Float  | PIB per cápita, es decir, el PIB ajustado al tamaño de la población                                   |
| `region`          | String | Región geográfica del país (por ejemplo, `"Latin America & Caribbean"`, `"East Asia & Pacific"`)      |
| `income_group`    | String | Clasificación del país según nivel de ingresos (por ejemplo, `"Low income"`, `"High income"`)         |


**Fuente de la variable externa**  
> [Per Capita GDP of All Countries 1970 to 2022](https://www.kaggle.com/datasets/dataanalyst001/per-capita-gdp-of-all-countries-1970-to-2022/data)  
> *(Kaggle)*

**Justificación :bulb:**  
- Se incorporó el **PIB per cápita** para complementar el PIB total, ya que este indicador refleja el desempeño económico ajustado por el tamaño de la población.  
- Permite comparar la riqueza relativa por habitante y entender mejor el nivel de vida y la productividad de cada país.  
- En conjunto con el PIB total, brinda una perspectiva más completa sobre el desarrollo económico y facilita la clasificación de los países en categorías (por ejemplo, *Low*, *Medium*, *High*).

**¿Por qué es útil? :chart_with_upwards_trend:**  
1. **Comparaciones Internacionales**: Ajustar por población hace más justa la comparación entre países de distinto tamaño.  
2. **Análisis Socioeconómico**: El PIB per cápita es un indicador clave para el bienestar y nivel de vida.  
3. **Modelos de Clasificación**: Clasificar a los países según rangos de PIB per cápita (por ejemplo, terciles) enriquece los modelos y la toma de decisiones.

**Integración en el Proyecto :sparkles:**  
- Se descargó el CSV con el PIB per cápita.  
- Se transformó a formato largo (usando `pd.melt`) para combinarlo con el DataFrame principal.  
- Se unificaron nombres de países y rangos de años para evitar valores `NaN`.  
- Se generó una sola tabla con tres fuentes de datos:  
  1. `gdp_data.csv` (PIB total)  
  2. `country_codes.csv` (regiones, ingresos, etc.)  
  3. *Per Capita GDP of All Countries* (PIB per cápita)  

Con esto, se logró un **DataFrame final** listo para el análisis, preprocesamiento y construcción de modelos de clasificación y regresión.


 
