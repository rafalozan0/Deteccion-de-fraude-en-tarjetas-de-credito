# Deteccion de fraude en tarjetas de credito
Es importante que las compañías de tarjetas de crédito puedan reconocer transacciones fraudulentas de tarjetas de crédito para que a los clientes no se les cobre por los artículos que no compraron.
# Nota:
Este modelo fue ejecutado con Azure notebooks, abrir el archivo
# Detector de anomaliasCC.ipynb
 
 # Contexto:
 Es importante que las compañías de tarjetas de crédito puedan reconocer transacciones fraudulentas de tarjetas de crédito para que a los clientes no se les cobre por los artículos que no compraron.
    
 # Contenido:
Los conjuntos de datos contienen transacciones realizadas con tarjetas de crédito en septiembre de 2013 por titulares de tarjetas europeos. Este conjunto de datos presenta transacciones que ocurrieron en dos días, donde tenemos 492 fraudes de 284,807 transacciones. El conjunto de datos está altamente desequilibrado, la clase positiva (fraudes) representa el 0.172% de todas las transacciones.

Contiene solo variables de entrada numéricas que son el resultado de una transformación PCA (Principal Component Analysis). Desafortunadamente, debido a problemas de confidencialidad, no podemos proporcionar las características originales y más información de fondo sobre los datos. Las características V1, V2, ... V28 son los componentes principales obtenidos con PCA, las únicas características que no se han transformado con PCA son 'Tiempo' y 'Cantidad'. La función 'Tiempo' contiene los segundos transcurridos entre cada transacción y la primera transacción en el conjunto de datos. La característica 'Cantidad' es la Cantidad de la transacción, esta característica se puede utilizar para el aprendizaje sensible al costo dependiente del ejemplo. La característica 'Clase' es la variable de respuesta y toma el valor 1 en caso de fraude y 0 en caso contrario.

 # Proposito:
 Identificar transacciones fraudulentas en tarjetas de credito.
 
 Dada la relación de desequilibrio de clase, recomendamos medir la precisión utilizando el área bajo la curva de precisión-recuperación (AUPRC). La precisión de la matriz de confusión no es significativa para la clasificación desequilibrada.
 
# Agradecimientos y creditos:
El conjunto de datos se ha recopilado y analizado durante una colaboración de investigación de Worldline y el Machine Learning Group (http://mlg.ulb.ac.be) de ULB (Université Libre de Bruxelles) sobre minería de datos grandes y detección de fraude. Más detalles sobre proyectos actuales y pasados sobre temas relacionados están disponibles en https://www.researchgate.net/project/Fraud-detection-5 y la página del proyecto DefeatFraud y a Krish C Naik creador del repositorio de donde fue tomado este modelo disponible en GitHub https://github.com/krishnaik06/Credit-Card-Fraudlent usado bajo la licencia GNU General Public License v3.0.
