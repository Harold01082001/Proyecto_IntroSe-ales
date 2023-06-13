# *Regresión de Datos*
 ----------------------------------------------------------------------------------------
<img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/f66d9252-be76-4771-92e0-050110d61c59" alt="Snow" style="width:60%">

---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Objetivo
### Tomando en cuenta la base da datos brindada, analizar la combinación de variables para hallar el valor de error. 

---------------------------------------------------------------------------------------------------------------
## Dataset
Los datos presentados son usados para entrenar el ventilador mecánico con una serie de gases y un pulmón artificial
Variables:
- Compliancia: C
- Resistencia pulmonar: RP
- Volumen de entrada: V_in 	
- Volumen de salida (real): V_out
- Diferencia de volumenes (V_out- V_in): Dif_vol
- Presión del ventilador generado por el analizador de gases: P_ventilador
- Presión PIP (manualmente): PIP
- Error aceptable generado por porcentaje de error del analizador de gases: Error_aceptable

 <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/03c85921-249d-417b-ae50-3e0b237f0028" alt="Snow" style="width:45%">
 
 
---------------------------------------------------------------------------------------------------------------
### Explicación de términos 


<img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/a7c2188e-3774-41c4-92c9-63e5fb37b339" alt="Snow" style="width:45%">

* Precisión: Proporción de casos positivos predichos correctamente sobre el total de casos positivos predichos. Por ejemplo: Cuantos datos de nuestro modelo que hemos dicho que son 0 son realmnte 0 --> "Valor" [1]
* Recall: Hace referencia a la sensibilidad. Proporción de casos positivos predichos correctamente sobre el total de casos positivos reales.
* f1-score: Combina recall y precision. Da una mejor visión del modelo y se puede visualizar la efectividad de la correlación
* Regresión: Predicción de nuevos valores basados en valores pasados (inferencia)
* Clasificación: Se basa en  la división de muestras en clases tomando en cuenta datos de entrenamiento
* Balanceo: Modificar la distribución original de la muestra, ya sea eliminando casos (undersampling) o replicando/creando nuevas muestras (oversampling)
---------------------------------------------------------------------------------------------------------------
## Consideraciones
* Se debe filtrar datos no deseados (eliminar filas o columnas de valores que no aportan en el análisis para evitar errores)
* Normalización: Para realizar cualquier tipo de regresión se necesita normalizar los términos
* Distribución de datos de entreamiento y datos de test: Para el modelo escogido se optó por 80% datos de entreamiento y 20% datos de test. Nos basamos en la bibliografía encontrada que garantiza esta distribución como la más precisa. [2]
---------------------------------------------------------------------------------------------------------------
## Procedimiento y resultados
* Visualizar el error aceptable para poder garantizar la calibración del ventilador (proporción o en conteo). Además, se grafica el desbalanceo de datos para un mejor entendimiento 
 <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/6edae283-3b59-4b44-8dc8-8f0712eff118" alt="Snow" style="width:65%">
 
* Se aplica la regresión logística a nuestros datos de entrenamiento en donde se genera la significancia. Recordar para que nuestro modelo sea correcto de necesita una significancia <= 0.05
* Para realizar esta regresión logística se necesita combinar dos variables. En este caso, hemos escogido analizar la variable "C" con las otras seis variables (no se considera el error aceptable generado como una variable). Se crea un array con todas las variables a comparar.
 <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/a4a4a4a2-86ff-4468-8e26-a9bfbd7d8a6b" alt="Snow" style="width:50%">
 
* Se analiza la significancia de cada combinación. En donde se obtienen dos pares con la significancia deseada. Para visualizar el valor de significancia de cada combinación revisar el código (el link se encuentra el final del md). Las variables con los resultados deseados son: 
  * "C" y "P_ventilador" 
  * "C" y "PIP" 
* Se elige una de estas combinaciones para  validar la efectividad del modelo mediante una validación cruzada, además de plotear la frontera de clafificación 
<img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/a350e548-ccf0-4d18-a541-009ff858db10" alt="Snow" style="width:70%">

* Realizar el sampleo para obtener la misma cantidad de datos de ambas variables y analizar nuevamente el cuadro de f1-score
---------------------------------------------------------------------------------------------------------------
#### * Link del código final: https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/L9%20-%20Regresi%C3%B3n%20de%20Datos%20(Introducci%C3%B3n%20a%20la%20inteligencia%20artificial)/Balanceo_ROS_IS_finalizado.ipynb
#### * Link para regresar a la carpeta de informes: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes
## Referencias 
- [1] De la Cruz, L., Meza, M., Venancio, J., & Cáceres, A. (2023). Diapositiva. Curso de Introducción a las señales biomédicas, Introducción a la inteligencia artificial, Perú.
- [2] García, J. (2021). Comparativa de técnicas de balanceo de datos. Aplicación en un caso real para predicción de fuga de clientes [Tarabajo de Fin de Máster inédita]. Universidad de Oviedo.
‌

‌


‌
