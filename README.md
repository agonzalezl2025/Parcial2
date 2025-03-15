# Parcial2

# Proyecto de Redes Neuronales

## Descripción
Este proyecto se centra en la construcción y optimización de modelos de redes neuronales para la clasificación de datos. Se trabajó con una base de datos de los países y su **GDP** desde **1960 hasta 2022**, implementando técnicas de limpieza, transformación y modelado avanzado.

# Diccionario
| **Variable**      | **Tipo**             | **Descripción**                                                                                 |
|-------------------|----------------------|-------------------------------------------------------------------------------------------------|
| `country_name`    | String              | Nombre oficial del país.                                                                        |
| `country_code`    | String              | Código (generalmente ISO) que identifica al país (ej: “AFG”, “ALB”).                             |
| `year`            | Entero              | Año calendario correspondiente al valor del PIB.                                                |
| `value`           | Numérico (float)    | Valor del PIB. Verificar la unidad (millones, miles de millones, etc.).                         |
| `region`          | String              | Región geográfica del país (ej: “Latin America & Caribbean”, “East Asia & Pacific”).             |
| `income_group`    | String              | Clasificación del país según nivel de ingreso (ej: “Low income”, “High income”).                |

## Integrantes del Equipo
- **David**: Responsable de la base de datos.
- **Lucas y Louis**: Desarrollo de redes neuronales.
- **Juan Fernando y Alejandro**: Redacción del README, relatoría y desarrollo de los bonos.

# Descripción del Proyecto

Este proyecto analiza la trayectoria de los países dentro de diferentes categorías económicas utilizando datos históricos del Producto Interno Bruto (PIB) desde 1960 hasta 2022. La clasificación de los países se basa en percentiles de riqueza mundial, dividiendo los datos en tres grupos:

30% superior: Países ricos

30% medio: Clase media

30% inferior: Países pobres

Con esta base de datos completa, se dividen los datos en dos conjuntos:

Entrenamiento (80%): Datos desde 1960 hasta 2012.

Prueba (20%): Datos de 2013 a 2022.

El objetivo del programa es predecir la clasificación de un país en 2022 dentro de las siguientes categorías: High, Upper Middle, Middle, Lower Middle y Low Income, utilizando modelos de redes neuronales.

Relatoría del Proyecto

# 1. Carga y Preparación de Datos

David fue el responsable principal de la carga y limpieza de los datos.

Se trabajó con Kaggle por primera vez, aprendiendo nuevas técnicas de gestión de datos.

Se integraron y limpiaron los datos en un solo diccionario para proceder con el análisis.

# 2. Limpieza y Distribución del Trabajo

Se confirmó que no había valores nulos en las bases de datos.

Distribución de tareas:

David: Manejo de la base de datos.

Lucas y Louis: Construcción de redes neuronales.

Juan Fernando y Alejandro: Redacción del README, relatoría y desarrollo de bonos.

Se documentaron los problemas encontrados en el proceso.

# 3. Reunión de Avance y Corrección de Errores

Se realizó una reunión de corrección de errores y ajustes en el modelo.

Se identificaron errores en la limpieza de datos, posteriormente corregidos.

Se integró una nueva base de datos de PIB per cápita.

# 4. Problemas y Soluciones en Redes Neuronales

Problemas Identificados

Baja precisión inicial del modelo (47%).

Hiperparámetros insuficientes para encontrar una configuración óptima.

Métrica de evaluación inadecuada (accuracy no era útil con clases desbalanceadas).

Soluciones Aplicadas

Expansión del espacio de hiperparámetros:

Ajuste de capas ocultas: (100,100), (150,100), (100,50,50).

Ampliación del rango de alpha y learning_rate.

Uso de validación cruzada con f1_macro en GridSearchCV.

Implementación de Early Stopping para evitar sobreentrenamiento.

Resultados:

Accuracy mejoró de 47% a 79%.

Optimización de la convergencia sin sobreajuste.

# 5. Problemas y Mejoras en el Modelo

Se encontró sobreajuste en el modelo, identificado por alta precisión en entrenamiento y baja en validación.

Se aplicaron mejoras:

Normalización de datos.

Reducción de la tasa de aprendizaje.

Uso de Dropout y L2 regularization.

Resultados:

La pérdida inicial se redujo de 168.8 a 34.4 y finalizó en 1.68.

La precisión de validación mejoró hasta 51.86%.

# 6. Desarrollo de los Bonos

Primer Bono: Integración de una Nueva Base de Datos

Se incluyó una base de datos adicional con PIB per cápita.

Se convirtieron variables numéricas en categóricas para mejorar la clasificación.

Segundo Bono: Análisis con SHAP y Waterfall Plot

Se implementó SHAP para explicar las predicciones del modelo.

Resultados:

Se identificó el impacto de cada variable en la clasificación de los países.

# 7. Conclusiones

La configuración inicial del modelo no era adecuada, lo que impedía el aprendizaje.

La optimización de hiperparámetros permitió alcanzar un accuracy del 70% en validación.

La inclusión de una nueva base de datos mejoró la clasificación de los países.

El uso de SHAP ayudó a comprender mejor la influencia de cada variable en el modelo.

Este proyecto representa un esfuerzo colaborativo para mejorar la clasificación económica de los países y proporcionar un modelo predictivo basado en datos históricos del PIB.

4. **Desarrollo del Bono**
   - Integración de una nueva base de datos con datos de PIB per cápita de los países entre 1960 y 2022.
   - Conversión de variables numéricas a categóricas para la clasificación.
   - Evaluación de los modelos con diferentes configuraciones.

## Problemas y Soluciones
### Problemas Técnicos
- **Dificultades en la limpieza de datos**
  - Solución: Corrección manual y automatización de transformaciones.

- **Sobreajuste del modelo**
  - Soluciones implementadas:
    - Reducción del **learning rate**.
    - Incremento del **dropout**.
    - Uso de **Regularización L2** y **EarlyStopping**.

- **Errores en la función de pérdida**
  - Se corrigió el uso de `MSE` a `categorical_crossentropy`, mejorando la precisión.

### Mejoras Implementadas
| Versión | Ajustes | Precisión Final |
|---------|---------|----------------|
| 1ra versión | Modelo inicial sin ajustes | 25% |
| 2da versión | BatchNormalization, reducción de learning rate, aumento de dropout | 72.84% |
| Versión final | StandardScaler, ajuste de pesos, reducción de dropout, ReduceLROnPlateau | 70% |

## Reuniones y Colaboración
- **Reunión de avance**: Corrección de errores y optimización de modelos.
- **Grabaciones de reuniones**: Compartidas en el grupo de WhatsApp.

## Conclusión
Este proyecto permitió mejorar significativamente la precisión de la red neuronal de un 47% a un **79%**, aplicando estrategias avanzadas de optimización. Se enfrentaron diversos desafíos técnicos, resolviendo problemas de sobreajuste y mala configuración del modelo. El trabajo colaborativo y el análisis iterativo fueron clave para alcanzar los resultados finales.


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


 
