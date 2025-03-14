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

#📂 Contenido del Proyecto

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
