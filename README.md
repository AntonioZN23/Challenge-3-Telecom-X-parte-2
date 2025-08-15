# Challenge-3-Telecom-X-parte-2

## Introducción
Se realizó una evaluación como científico de datos junior en la empresa Telecom X dentro del proyecto "Churn de Clientes". Mediante el presente proyecto se busca generar un modelo de ML capaz de determinar las causas del alto índice de abandono de los clientes al realizar para generar estrategias correctivas, así como un modelo capaz de predecir el abandono de los clientes en función de sus características, para lo cual fue proporcionada una base de datos de la empresa, la cual pasó por un procedimiento de ETL para poder ser analizada.  
________________________________________________________________________________

## Tratamiento de datos
La información proporcionada fue mediante un documento JSON, el método de extracción fue realizado utilizando la librería Pandas para la generación del Data Frame (DF). El DF resultante requirió un tratamiento para el acomodo de los diccionarios dentro de las distintas columnas, así como el manejo de información faltante en la columna 'Churn', se optó por eliminar esta información indeterminada constataba menos del 5% general y resultaba irrelevante para el análisis.

Posteriormente, se le realizó un tratamiento a los distintos tipos del DF con la finalidad de mantener una mayor legibilidad al transformar objetos a valores enteros y flotantes, de esta manera en futuros análisis el procesamiento de la información resultará más directo y al tener un mismo térmio para valores de sí = 1 y no = 0, se facilita el entendimiento del DF.

Finalmente, se realizó una codificación de las categorías con respuestas más allá del sí o no, de este modo características como el tipo de servicio de internet cuentan con un formato según la respuesta que no da mayor peso a una respuesta u otra, así al entranar al modelo de ML, este no estará sesgado por una codificación errónea. 
________________________________________________________________________________

## Información obtenida

A lo largo del presente reporte se han realizado observaciones en la información que corroboran la hipótesis propuesta en el primer informe realizado a la compañía Telecom X, donde se estableció que las variables con mayor impacto en la decisión de los clientes para abandonar o no la empresa radica en el tipo de contrato, el tiempo de tenencia del servicio, así como los cargos totales y mensuales, entre otros.

A partir de la generación de modelos de Machine Learning de tipo categóricos, específicamente los modelos de árbol y bosque aleatorio, se estableció que las principales variables que influyen en la predicción de la estadía o abandono de un cliente es principalmente atribuible al tipo de contrato, el tiempo, los cargos y el tipo de servicio de internet. Lo de que demuestra que si el cliente cuenta con un contrato de mes a mes, tiene un tiempo de tenencia baja, los cargos totales son bajos pero cuenta con cargos mes a mes mayores, y además, cuenta con servicio de internet de fibra óptica, la tendencia será el abandono de la empresa.

Ante esta situación las acciones que se deberán tomar para retener a los clientes radica en la generación de un programa de fidelidad que resulte más atractivo a los clientes, de este modo, se busca que aquellos clientes con contrato mes a mes reduzcan su índice de deserción y de ser posible, se deberá buscar que los clientes en este campo migren a planes de mayor tiempo, los cuales cuentan con menor impacto al momento de determinar si un cliente abandonará o no la empresa.

La siguiente acción a tomar para retener a los clientes es la mejora del sistema de fibra óptica, pues se observó que los clientes que cuentan con este servicio tienen mayor tendencia a abandonar la empresa, lo cual implica que no se encuentran conformes con la calidad del servicio proporcionado.

Para resolver el abandono de los clientes de poco tiempo en la empresa, se deberá generar promociones que resulten atractivas para los nuevos clientes, de tal modo que su estadía supere los primeros meses cuando existe una mayor cantidad de deserción.

Se generó un modelo capaz de predecir con éxito en un 79% si los clientes podrían abandonar o no la empresa, se propone implementar este modelo para buscar retener al cliente mediante promociones y programas.

Teniendo en mente las variables que mayormente influyen en la determinación del abandono o estadía de los clientes, así como las acciones a tomar, se procede a hablar sobre los modelos generados para funcionar como un apoyo a la empresa. En primera instancia es importante mencionar que se generaron 4 modelos predictivos y una línea base, el desempeño de estos modelos es 79% para un modelo de árbol de clasificación, 76% para el modelo de KNN, 29% para un bosque aleatorio optimizado y 33% para un bosque aleatorio sin optimizar, finalmente se cuenta con un rendimiento del 73% para la línea base.

De esta manera, se establece que el mejor modelo realizado para la predicción de una potencial deserción de un cliente es un modelo de árbol de clasificación, pues es el modelo que cuenta con una mayor aproximación. 
