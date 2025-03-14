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


# Relatoría

# La Aventura de los Cinco Enanitos y el Gran Código Perdido

En lo profundo del Bosque Digital, vivían cinco enanitos muy trabajadores: David el Ingenioso, Lucas el Sabio, Louis el Curioso, Juan Fernando el Escritor y Alejandro el Organizado. Juntos, emprendieron una misión épica: construir la Gran Red de Neuronas del Bosque utilizando datos mágicos dispersos en pergaminos electrónicos.

# 🏰 El Desafío Comienza

Todo comenzó cuando los enanitos decidieron unir fuerzas para subir y organizar los misteriosos datos del Bosque Digital. David el Ingenioso tomó la delantera, asegurándose de que las bases de datos fueran subidas correctamente.

Sin embargo, la tarea no fue sencilla. Pronto se dieron cuenta de que los datos estaban divididos en dos partes y juntarlas era un verdadero rompecabezas. Pero no se dieron por vencidos y, tras varios intentos, lograron fusionarlas en un solo Gran Diccionario de Datos.

# 🔎 El Arte de la Limpieza

Con los datos ya unidos, los enanitos se enfrentaron a su siguiente reto: limpiar los datos. Para ello, tuvieron que eliminar errores, corregir inconsistencias y preparar todo para la siguiente fase de su aventura.

Una vez que la limpieza estuvo completa, se reunieron en el Gran Claro del Bosque para dividir las tareas:

David el Ingenioso se encargaría de seguir organizando la base de datos.

Lucas el Sabio y Louis el Curioso trabajarían en la construcción de la Red de Neuronas.

Juan Fernando el Escritor y Alejandro el Organizado se encargarían de documentar todo y preparar los bonos mágicos.

# 📜 Un Nuevo Problema Surge

Mientras trabajaban en el Gran Cuadernillo del Código, los enanitos descubrieron que debían documentar las dificultades que encontraron. David, Lucas y Louis escribieron sobre los problemas más desafiantes:

La compleja categorización de los años y percentiles.

El mal funcionamiento del encantamiento de One-Hot Encoding, que solo mostraba "True" y "False".

La conversión de las variables X y Y de cadenas de texto a números.

Pero lo peor aún estaba por venir…

Analsis de datos 1D 

El predispuesto de gdp income que podía dañar las predicciones

Las separaciones en 30% para equilibrar los datos entre los High y médium 

Consejo: aplique OneHotEncoder a y_train_class y y_test_class luego de crear la variable
categórica. El resultado final debería verse así: no nos hizo falta p
 rque ya lo separamos por cada año

Nos dimos cuenta que era mejor normalizar 

Para el 3a debe de ser de una sola dimensión el Y pero para el 3b debe de ser de varias

# 🤯 El Gran Error

Justo cuando creían que todo iba bien, descubrieron un error en la limpieza de datos. ¡El hechizo no había funcionado como esperaban! Tuvieron que corregirlo antes de poder construir la Gran Red de Neuronas. Además, el bono mágico era más difícil de lo que imaginaban. Pensaron que incluía todo el Anexo Mágico, pero tras consultarlo con el sabio Camilo, descubrieron que solo debían agregar otra base de datos.

# 🛠 La Última Batalla

Los enanitos encontraron una nueva base de datos sobre el PIB per cápita y trabajaron duro para integrarla correctamente. Tras muchas pruebas y errores, lograron que todo encajara como dictaban las Instrucciones del Anexo Sagrado.

A la hora pactada, se reunieron en el Gran Claro Digital donde Louis y Lucas mostraron su progreso. Después de revisar el código y corregir errores, decidieron dividirse nuevamente:

David el Ingenioso trabajaría en el Bono del Punto 3.

Louis y Lucas se encargarían de los bonos del Punto 2.

Juan Fernando y Alejandro se ocuparían del Bono del Anexo.

# 🎉 La Misión Cumplida

Así, cada enanito tomó su tarea y se puso a trabajar con entusiasmo. Después de largas horas de esfuerzo, la Gran Red de Neuronas del Bosque quedó lista y funcionando. Los cinco enanitos celebraron su éxito, sabiendo que habían superado cada obstáculo con ingenio, trabajo en equipo y un poco de magia digital.

Y así, su historia quedó escrita en los anales del Bosque Digital… hasta su próxima gran aventura. 🚀
 
