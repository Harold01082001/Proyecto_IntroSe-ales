# *Entregable para la clase (Algoritmo de detección QRS)*
 ----------------------------------------------------------------------------------------
## Tabla de contenidos 
------------------------------------------------------------------------------------------------
- [Procedimiento](#Procedimiento)
- [ECG Breve Explicación](#ECG-Breve-Explicación)
   * [Complejos QRS](#Complejos-QRS)
- [Filtros Notch](#Filtros-Notch)
- [Frecuencias ECG](#Rango-de-frecuencias-de-las-señales-en-el-ECG)
- [Referencias](#Referencias)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Procedimiento
* 1. Se lee el DataSet
* 2. Se analiza el ECG en frecuencia  (se detecta los ruidos en 50 Hz y 150 Hz)
* 3. Se reducen los ruidos con filtro Notch
* 4. Se filtra la señal con un filtro pasa banda
* 5. Se filtra la señal con un filtro pasa alto
* 6. Se realiza el filtrado derivativo
* 7. Se eleva al cuadrado la señal
* 8. Se emplea el operador Moving Window Integration
* 9. Se marcan los picos
* 10. Se realiza el análisis de Threshold: se halla el umbral del pico R y ruidos
* 11. Se obtienen los complejos QRS en la señal ECG inicial

---------------------------------------------------------------------------------------------------------------
## ECG Breve Explicación
El electrocardiograma es un registro de la actividad eléctrica del corazón. Esta es una prueba no invasiva que mide la regularidad de los latidos, la frecuencia cardíaca y detecta posibles anomalías que se puedan dar en la conducción eléctrica del corazón. Por ejemplo, arritmias, enfermedad de las arterias coronarias, si el paciente ha tenido un ataque cardíaco anteriormente, entre otros. En general, es una herramienta esencial para la monitorización y diagnóstico de afecciones cardiovasculares y es muy común su uso clínico[1].

<p align="center">
  <img width="350" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ecg.jpg">
</p>

### Complejos QRS 
Asimismo, los electrocardiogramas tienen distintas ondas, segmentos y un complejo que representan aspectos de la actividad eléctrica del corazón. Entre las ondas se pueden encontrar la onda P, Q, R, S y T. En los segmentos se tienen al P-R, Q-T, S-T y P.  Finalmente, está el complejo QRS, el cual representa la despolarización ventricular por la contracción que se da entre los ventrículos del corazón. Como su nombre lo indica, está compuesto por 3 ondas: Q, R y S. En este complejo, la onda Q representa una deflexión negativa inicial, posteriormente la onda R es una deflexión positiva y por último la onda S es nuevamente una deflexión negativa [2]. La duración promedio del complejo no debería exceder los 120 milisegundos (0,12 segundos). Si es que este tiempo es mayor, podría evidenciar ciertos trastornos en la conducción que serían importantes para encontrar anomalías o deficiencias en el funcionamiento. [3]

<p align="center">
  <img width="500" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/PQRS.jpg">
</p>

## Filtros Notch
Los filtros Notch son un tipo de filtro que se suele usar para el procesamiento de señales. Estos se basan principalmente en la eliminación o reducción de posibles interferencias y generan una gran atenuación en la respuesta correspondiente a la frecuencia específica o no deseada. Esto a su vez permite que las frecuencias que se encontraban cercanas y que sí son de interés, no sufran alteraciones significativas y que conserven su información relevante [4].
Se podría deducir que los filtros Notch son utilizados en los ECG para ayudar a eliminar ciertas interferencias y mejorar la precisión de los resultados con la finalidad de poder detectar con mayor facilidad los patrones cardíacos y posibles anomalías [5].

### Rango de frecuencias de las señales en el ECG
Una señal electrocardiográfica consiste en una sucesión de ondas y se caracteriza por tener una amplitud que oscila entre 0.5 y 5.5 mV, así como un ancho de banda comprendido entre 0.01 y 250 Hz. Los complejos QRS ocupan la zona alrededor de los 17 Hz, teniendo una distribución espectral de la energía que depende del tipo de latido.[6] Debido a su amplitud extremadamente baja, la señal electrocardiográfica está expuesta a diversas interferencias, siendo la interferencia eléctrica (conocida como ruido de 60 Hz) una de las más comunes. En frecuencias bajas, existe la presencia de ruidos (inferiores a 0.5 Hz) generados por los movimientos del paciente, artefactos musculares o interferencias eléctricas. [7][8]

###  Filtro derivativo 
El filtro derivativo es un tipo de filtro que al calcular las derivadas de los datos en función a su modelo de interpolación, puede utilizarse para reducir el ruido. Los datos a los que se puede someter este filtro son imágenes, datos, matrices o audios [9]. 
En nuestro caso, ya que estamos revisando la información que nos brinda un ecg hemos investigado que mayormente para el análisis del complejo QRS se utiliza un algoritmo de detección basado en la primera derivada. Este método basado en la primera derivada se utiliza más que todo en el análisis en tiempo real o en un gran número de datos ya que sus cálculos no suelen ser extensos [10]. 

### Moving window integration 

El uso del "comando" moving window es un proceso por el cual se calcula un valor promedio para un contorno de valores en celdas específicas, las funciones que usualmente se calculan para esta sección de valores son suma, media, mínimo, máximo, entre otras [11].  Con respecto a su relación con el ECG, su propósito es obtener la mayor información de las características de la forma de la onda como su pendiente en la onda R. Como vimos en el ítem anterior, ya que la señal pasará por un filtro derivativo la salida va a presentar múltiples picos, por lo que al integrar esta ventana se podrá ordenar las características y analizar la información importante del complejo QRS  [12].

#### Link del código: https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/L7-%20Algoritmo%20de%20detecci%C3%B3n%20QRS/Prueba_ECG_S8.ipynb
#### Regresar a la carpeta de informes: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes

## Interpretación de resultados
Como se puede observar en la imagen el filtrado diseñado , en este caso un pasabanda, logra eliminar el ruido generado por la frecuencia de la fuente de alimentación alterna. El pasabanda fue realizado a base de un filtro pasa-alta y un pasa-baja, donde sacamos dos frecuencias de corte. Para poder demostrar el efecto tomamos como modelos la señal ECG en reposo. 
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal Orgininal (Reposo 1)</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/fb085676-2a77-42e5-b5c1-529f9b043641" alt="Snow" style="width:90%">
  </div></th>
            <th><div class="column">
                <p>Señal aplicando el filtro pasa banda (Reposo 1)</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/377c21b8-fae9-4641-875d-60b6c0323e7b" alt="Snow" style="width:90%"></th>  
  </table>
 </p>


Por otro lado, con respecto al operador cuadrático con el anterior procedimiento (filtrado), nos permite detectar las zonas de mayor amplitud , que en nuestros caso sería la sección de la onda R. Esta zona será la que más adelante vamos a analizar (onda R) ya que es la que se asocia a un fallo valvular. En este caso, hemos evaluado la señal ECG en reposo

 <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/d40d2422-0261-4dec-a878-443f54aacfee" alt="Snow" style="width:90%">



## Referencias 
- [1] “Electrocardiogram (ECG or EKG) - Mayo Clinic,” Mayoclinic.org, 2022. https://www.mayoclinic.org/es-es/tests-procedures/ekg/about/pac-20384983 (accessed May 18, 2023).
- [2] L. Azcona, “Estructura del corazón Capítulo 4 El electrocardiograma.” Available: https://www.fbbva.es/microsites/salud_cardio/mult/fbbva_libroCorazon_cap4.pdf
- [3] N. Siles, J. Schmidberg, R. Acunzo, M. Elizari, and P. Chiale, “Diagnóstico electrocardiográfico de los bloqueos intraventriculares y auriculoventriculares.” Available: https://www.siacardio.com/wp-content/uploads/2015/01/ECG-Capitulo-2-Diagnostico-electrocardiografico-de-los-Bloqueos-IV-y-AV.pdf
- [4] “Filtro Notch,” Scribd, 2023. https://es.scribd.com/doc/92778715/Filtro-Notch (accessed May 18, 2023).
- [5] “ANÁLISIS DE ESQUEMAS DE FILTRADO PARA SEÑALES ELECTROCARDIOGRÁFICA (ECG) LEYDY LAURA ÁLVAREZ ESCOBAR UNIVERSIDAD TECNOLÓGICA DE PEREIRA FACULTAD DE TECNOLOGÍAS ESCUELA DE TECNOLOGÍA ELÉCTRICA PEREIRA 2007.” Available: https://core.ac.uk/download/71395502.pdf
- [6] ECG-FUNDAMENTOS TEÓRICOS. (2023). Curso de Instrumentación Biomédica (Universidad Peruana Cayetano Heredia), (Clase ECG), 6.
- [7] Claros, D., Minaya, J., & Perez, D. (2019). Diseño de un Electrocardiograma (ECG). Universidad de Ingeniería y Tecnología, Lima, Perú.
- [8] Cárcamo, L. M., Osorio, F., & Villegas, J. (2020). Diseño de aplicación prototipo para la detección y clasificación de arritmia usando métodos de machine learning a partir de ECGs. Handle Proxy. http://hdl.handle.net/10584/9273
- [9]“DerivativeFilter—Wolfram Language Documentation,” Wolfram.com, 2014. [Online]. Available: https://reference.wolfram.com/language/ref/DerivativeFilter.html#:~:text=DerivativeFilter%20is%20a%20linear%20filter,to%20reduce%20susceptibility%20to%20noise. [Accessed: May 24, 2023]
- [10]N. M. Arzeno, Z. Deng, and C.-S. Poon, “Analysis of First-Derivative Based QRS Detection Algorithms,” vol. 55, no. 2, pp. 478–484, Jan. 2008, doi: https://doi.org/10.1109/tbme.2007.912658. [Online]. Available: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2532677/. [Accessed: May 24, 2023]
- [11]“Moving Windows in R: Rectangles, Circles, and Zeros...Oh my! – Biogeography & Landscape Dynamics Lab,” Assallab.org, 2019. [Online]. Available: https://assallab.org/blog/moving-windows-in-r. [Accessed: May 24, 2023]
- [12]A. Aishwarya, B. N. S, M. Swathi, and P. Ravi, “Detection of Obstructive Sleep Apnoea Using ECG Signal,” ResearchGate, Mar. 08, 2013. [Online]. Available: https://www.researchgate.net/publication/299730947_Detection_of_Obstructive_Sleep_Apnoea_Using_ECG_Signal#pf20. [Accessed: May 24, 2023]
‌
‌
‌

‌


‌
