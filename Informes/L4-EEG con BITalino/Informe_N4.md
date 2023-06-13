# *Informe de Laboratorio 4*
 ----------------------------------------------------------------------------------------
## Tabla de contenidos 
------------------------------------------------------------------------------------------------
- [Objetivos del laboratorio](#Objetivos-del-Laboratorio)
- [Materiales](#Materiales-utilizados)
- [Electroencefalograma](#Electroencefalograma)
- [Actividades del laboratorio](#Actividades-del-laboratorio)
   * [Actividad 1](#Actividad-1-del-laboratorio)
   * [Actividad 2](#Actividad-2-del-laboratorio)
- [Referencias](#Referencias)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Objetivos del Laboratorio
- Adquirir señales biomédicas de EEG.
- Hacer una correcta configuración de BITalino. 
- Extraer la información de las señales EEG mediante el software OpenSignals (r)evolution.
- Extraer la información de las señales EEG mediante el software OpenBCI GUI
---------------------------------------------------------------------------------------------------------------
## Materiales utilizados

### Medición usando BITalino 
<p>
    <table>
        <tr>
            <th> 1x Sensor Electroencefalograma Ensamblado en el BITalino</th>
            <th> 3x Electrodos</th>
            <th> 1x Cable para los electrodos </th>
         </tr>
    </table>
        </p>
<p align="center">
  <img width="200" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/materiales_lab4.jpg">
</p>

### Medición usando Ultracórtex Mark IV

#### Partes Impresas:
<p>
    <table>
        <tr>
            <th> 1 x Marco (parte delantera + parte trasera)</th>
            <th> 35 x Mech_Parts </th>
            <th> 2 x Cubiertas </th>
    </table>
        </p>
<p align="center">
  <img width="400" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/PartesImpresas.jpg">
</p>

#### Partes Externas:
<p>
    <table>
        <tr>
            <th> 1 x Tornillo de plástico (parte delantera + parte trasera)
            <p align="center">
            <img width="50" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/tornillo.jpg">
            </p></th>       
            <th> 6 x Unidades Puntiagudas
            <p align="center">
            <img width="150" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/puntiagudas.jpg">
            </p></th> 
            <th> 2 x Electrodos Secos (No puntiagudos)
            <p align="center">
            <img width="50" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/electrodos.jpg">
            </p></th> 
            <th> 5 x Unidades de Confort
            <p align="center">
            <img width="150" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/confort.jpg">
            </p></th> 
            <th> 2 x Clip para la oreja
            <p align="center">
            <img width="50" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/clips.jpg">
            </p></th> 
            <th> 1 x Placa OpenBCI Cyton de 8 canales
            <p align="center">
            <img width="50" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/cyton8.jpg">
            </p></th> 
            <th> 1 x Batería recargable de iones de litio + Cargador para Batería
            <p align="center">
            <img width="150" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/BateriaCargador.jpg">
            </p></th> 
    </table>
        </p>

## Electroencefalograma 
<p align="center">
  <img width="300" height="200" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/electroencefalograma.jpg">
</p>


 ### _¿Qué representa un EEG?_ 

El EEG representa el estudio de la señal eléctrica del cerebro, la cual se mide con pequeños electrodos colocados en la cabeza. La señal eléctrica es generada por el potencial postsináptico, la cual solo toma pequeños milisegundos. [1]

### _¿Como se funciona el cerebro para que se de el EEG?_
El cerebro cuenta con 4 lóbulos : frontal (naranja), temporal (verde), parietal (azul), occipital (amarillo); los cuales tienen distintas funciones. El lóbulo frontal se encarga de los movimientos voluntarios, la toma de decisiones, los procesos congnitivos, tambien la concentración y la personalidad. Por otro lado, el lóbulo temporal se encarga de los procesos sensoriales , de la memoria a largo plazo,  la memoria visual como tambien en las emociones y el lenguaje. En cuanto al lóbulo parietal, este se encarga de la relación entre el ambiente y el cuerpo, más en específico la coordinación de las partes del cuerpo al realizar los movimientos. Por último, el lóbulo occipital , este es responsable de los procesos visuales [2].

<p align="center">
  <img width="400" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/CerebroLobe.jpg">
</p>

### _Señales del EEG_
Tenemos 5 posibles señales en un EEG, las cuales van a depender de acuerdo a la acción. Acontinuación las mostramos en un gráfico y las especificamos a detalle [2]. 

<p align="center">
  <img width="600" height="500" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/RangoOndas.jpg">
</p>

#### Gamma: se da a una frecuencia mayor a 25Hz y ocurre cuando se esta concentrado o resolviendo problemas. 

#### Beta: la oscilación se da en un rango de 12-25 Hz y la señal representa la mente activa como ocupada, en el caso que la concentración sea mayor la oscilacion va a aumentar. 

#### Alpha: la oscilación se da en un rango de 8-12 Hz, esta representa la función de la memoria, el motor y la parte sensorial. Un caso especial es cuando estamos con los ojos cerrados el poder de las bandas se incrementa, lo cual luego se suprime cuando se cierran los ojos. 

#### Theta: la oscilación se da en un rango de 4-8 Hz , se origina gracias al lado derecho del cerebro, la señal puede indicar somnolencia. 

#### Delta: la oscilación se da en un rango de 0-4 Hz y se genera en las diferentes fases del sueño, la amplitud de la señal dependera de la profundidad del sueño. 

### _Adquisición de las señales de un EEG_

La medición y adquisición de las señales del electroencefalograma se realiza utilizando el
Sistema Internacional de Posicionamiento 10/2. Para saber los puntos específicos para
colocarlos, se debe hacer una medición de la longitud entre el nasion e inion. Dicha
longitud se debe dividir en segmentos proporcionales a ciertos porcentajes. La división debe
ser de la siguiente manera: 10% - 20% - 20% - 20% - 20% - 10%. Estos segmentos pueden
medir entre 3 y 6 cm dependiendo del tamaño de la cabeza del paciente. Estas mismas
proporciones se utilizarán del lado inverso entre oreja y oreja. [3] [4]

Adicionalmente, es importante conocer la nomenclatura de los electrodos. Esta depende de
la topografía del cerebro. [3] [4]
- Parte frontal: F
- Parte parietal: P
- Parte occipital: O
- Parte central: C
- Parte temporal: T

Acontinuación se muestra la imagen de la distribución del espacio de los electrodos según Sistema Internacional 10/20 [3]

<p align="center">
  <img width="400" height="200" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/espacio_electrodos.jpg">
</p>

Asimismo, estas letras que se colocan van acompañadas de un número, los cuales hacen
referencia a un hemisferio cerebral. [3] [4]
- Números pares: hemisferio derecho
- Números impares: hemisferio izquierdo

Para ejemplificar esta información esta la siguiente figura que representa el posicionamiento de los electrodos según Sistema Internacional 10/20 [3]

<p align="center">
  <img width="300" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/posicion_electrodos.jpg">
</p>

### _Aplicaciones del EEG_
El EEG se utiliza para el diagnostico de desordenes o enfermedades del cerebro, ya que con el se puede detectar los cambios en su actividad. A continuación mencionamos ejemplos de diagnostico gracias al EEG [1]  

 * Tumores cerebrales
 * Daños o disfunciones cerebrales (encefalopatías)
 * Trastornos del sueño
 * Accidente cerebrovascular


## Actividades del laboratorio
Para el presente laboratorio registraremos las señales del cerebro en distintas situaciones mediante el uso del bitalino y OpenBCI; además, las compararemos e interpretaremos.

## Actividad 1 del laboratorio
La primera actividad consiste en las lecturas de las señales del cerebro en tres distintas situaciones: señal con los ojos cerrados, señal mientras se realiza una actividad matemática y por último, señal durante un ejercicio de memoria.

### Conexiones usadas
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Electrodos-Cabeza (vista frontal)</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/conexiones_lab4.jpg" alt="Snow" style="width:55%">
  </div></th>
            <th><div class="column">
                <p>Electrodos-Cabeza (vista lateral)</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/conexion_2.jpg" alt="Forest" style="width:55%"></th>
    </table>
 </p>



### Lectura de la señal en una actividad de reposo
Para la primera lectura se realizan cinco repetiones de 5 segundos cada una en la que se abren y se cierran los ojos. La señal que se obtennga de las mediciones debería mostrar una onda sin muchas oscilaciones, en este caso algo similar a la onda tipo Alpha. 

<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal en actividad de reposo</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ojos_cerrados_señal.jpg" alt="Snow" style="width:60%">
  </div></th>
            <th><div class="column">
                <p>Video de la toma de la señal </p>
    <video src="https://user-images.githubusercontent.com/128879214/233190177-0f269d79-0848-4820-a0f3-d67c99122691.mp4" alt="Forest" ></video></th>
    </table>
 </p>

### Lectura de la señal mientras se realiza una actividad matemática
Para la segunda actividad se preguntaron cuatro problemas de matemática sencillos en un tiempo de 12 segundos. La señal esperada debería resultar algo similar a la onda de tipo Beta o Gamma ya que la mente se encuentra activa resolviendo problemas.

<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal en la actividad</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/matematica.jpg" alt="Snow" style="width:75%">
  </div></th>
            <th><div class="column">
                <p>Video de la toma de la señal </p>
    <video src="https://user-images.githubusercontent.com/128879214/233192823-ba6276dd-0310-4f6c-ada7-db7b4f493165.mp4" alt="Forest" ></video></th>
    </table>
 </p>


### Lectura de la señal mientras se realiza una actividad de memoria 
La última actividad consistio en un ejercicio de memoria, el cual constaba de recordar cinco palabras luego de cinco minutos, en este caso las palabras a recordar fueron : fantasía, tetris, meditación, Elena y conductividad. La señal esperada debería resultar semejante a la onda Gamma, ya que se esta en un estado de concentración.

<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal en la actividad</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/memoria.jpg" alt="Snow" style="width:75%">
  </div></th>
            <th><div class="column">
                <p>Video de la toma de la señal </p>
    <video src="https://user-images.githubusercontent.com/128879214/233192681-aea659cd-e1b9-4bb6-ac22-a6fe97ceb1a2.mp4" alt="Forest" ></video></th>
    </table>
 </p>

 

## Interpretación de la primera actividad 
En esta sección analizamos lo ocurrido con la actividad cerebral de la compañera Vanessa Diaz Arrascue, quien realizó las actividades que se indicaban. El programa de OpenSignals que permite trabajar con BITalino captó las señales provenientes del electrodo colocado como se presenta en la imagen.

<p align="center">
  <img width="400" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/cabeza.jpg">
</p>

Desde una simple inspección sobre las gráficas para los 5 diferentes momentos, podemos observar que la actividad rítmica para los momentos en los cuales se cierra los ojos y se mantiene una posición de reposo está modulada de tal manera que los picos prominentes son puntuales (>900 uV) y en la mayor parte del tiempo se encuentra la señal con amplitudes no mayores a los 800 uV. Es más interesante analizar la señal proveniente del momento de actividad cerebral cuando se realizan las cinco preguntas matemáticas. Se observa que la actividad cerebral proveniente de la parte frontal del cerebro aumenta drásticamente y de manera intermitente; es decir que constantemente los picos llegan a amplitudes entre los 1000 uV. Por último, la señal proveniente del recordar de las cinco palabras complejas evidencia que en ciertos momentos de la gráfica los picos aumentan a la amplitud de aproximadamente 100 uV, siendo una especulación que en dichos momentos el cerebro realiza una actividad conjunta para mandar el impulso sobre la respuesta a la palabra que, en el inmediato, va a nombrar. Según Morillo,L. corrobora que, en el análisis de las bandas alfa (bandas que el BITalino analiza) corresponden a la actividad cerebral en alerta, así como permite evaluar las funciones reflejas relacionadas a la memoria, actividad motora y la actividad sensorial. [5]. Un comentario adicional para tomar en cuenta es la presencia de artefactos y ruido que puede afectar la medición de las gráficas del electroencefalograma; más específicamente nos referimos al ruido generado por la actividad motora de la mandíbula o músculos oculares que también generan impulsos eléctricos.

<p>
    <table>
        <tr>
            <th><div class="column">
                <p>EEG 1</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/eeg_1.jpg" alt="Snow" style="width:90%">
  </div></th>
            <th><div class="column">
                <p>EEG 2</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/eeg_2.jpg" alt="Forest" style="width:90%"></th>
    
<th><div class="column">
                <p>EEG 3</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/eeg_3.jpg" alt="Forest" style="width:90%"></th>
    
<th><div class="column">
                <p>EEG 4</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/eeg_4.jpg" alt="Forest" style="width:90%"></th>
    
<th><div class="column">
                <p>EEG 5</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/eeg_5.jpg" alt="Forest" style="width:90%"></th>
    

  </table>
 </p>
 
## Actividad 2 del laboratorio
Para la segunda actividad de laboratorio utilizamos la plataforma Open BCI, la cual consiste en una interfaz entre el cerebro y la computadora para poder simular señales de electroencefalograma y poder analizar e interpretar la actividad del cerebro. El dispositivo específico que se utilizó como casco con electrodos fue el “Ultracortex Mark IV EEG Headset”, el cual funciona con el sistema de posicionamiento mencionado anteriormente. [6] Este casco puede ser impreso en 3D y se va adecuando a los distintos tamaños que puede tener la cabeza de la persona que lo utiliza. A diferencia de otros programas utilizados como el Open Signals, el Open BCI provee información sobre las señales correspondientes a las 5 bandas de frecuencia (delta, theta, alpha o mu, beta y gamma). [7].

<p align="center">
  <img width="500" height="350" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/casco.jpg">
</p>

De acuerdo al sistema 10/20, los electrodos azules serán correspondientes a 8 canales por
“default” de acuerdo a la plataforma Open BCI [8]:

- Canal 1(N1P) - Fp1
- Canal 2(N2P) - Fp2
- Canal 3(N3P) - C3
- Canal 4(N4P) - C4
- Canal 5(N5P) - P7
- Canal 6(N6P) - P8
- Canal 7(N7P) - O1
- Canal 8(N8P) - O2

Para entender mejor esto mostramos una figura con la  distribución de los electrodos azules correspondientes a los 8 canales [8]

<p align="center">
  <img width="400" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/canales.jpg">
</p>

Para obtener señales con la mejor calidad posible cuando se trabaja con sensores
encefalográficos, hay ciertos factores que pueden alterar los resultados y se presentan a
continuación [9]:
- El ambiente debe ser apropiado para la realización de la toma, teniendo en cuenta
que mientras menos ruido y distracciones haya, los resultados serán más precisos,
- Los movimientos faciales que realice el paciente se verán reflejados en la señal. Ya
sea cerrar o abrir los ojos, fruncir el ceño, masticar, guiñar el ojo, entre otros.
- La diferencia de luz que puede haber en el ambiente.

#### - Aclaración: En esta actividad se realiza un análisis continuo de las pruebas realizadas en la actividad 1


### Conexiones usadas
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Marco-Cabeza (vista frontal)</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/VaneMark.jpg" alt="Snow" style="width:40%">
  </div></th>
            <th><div class="column">
                <p>Marco-Cabeza (vista lateral)</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/VaneMarkl.jpg" alt="Snow" style="width:95%"></th>
    </table>
 </p>

### Explicación de cada actividad realizada + Video de la captura de la señal
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>En la primera actividad nuestra compañera se mantuvo en reposo por 20 segundos, con los ojos completamente cerrados evitando cualquier tipo de distracción. Las señales obtenidas no deben presentar muchas oscilaciones</p>
    <video src="https://user-images.githubusercontent.com/43499263/233392533-bf3f22a1-ed2d-4aec-8f51-6427797bcb78.mp4" alt="Forest" style="width:30%" ></video>
  </div></th>
            <th><div class="column">
                <p>En la segunda actividad se le pidió a nuestra compañera parpadear 5 veces con intervalos de 5 segundos. Se puede comenzar a notar ciertas oscilaciones pero no son tan proporcionales</p>
    <video src="https://user-images.githubusercontent.com/43499263/233395296-06393317-7764-456d-8017-2261d6a2e232.mp4" alt="Forest" style="width:30%"> </video>
  </div></th>
           <th><div class="column">
                <p>La última actividad consistió en pedirle a nuestra compañera que recuerde la serie de palabras mencionadas en la actividad 1. En esta actividad se puede notar que el esfuerzo se refleja en oscilaciones de las ondas en los distintos canales </p>
   <video src="https://user-images.githubusercontent.com/43499263/233396802-1f641721-fd25-4e16-96f0-c050fc329e87.mp4" alt="Forest" style="width:30%"></video>
  </div></th>
  </table>
 </p>
 
## Interpretación de la segunda actividad  
#### > Señal obtenida en OpenBCI GUI:
<img src="https://user-images.githubusercontent.com/43499263/233399735-36db0281-06e5-4285-9e90-9df28ff7029a.jpg" alt="Snow" style="width:50%"></th>

#### Aclaración: Los ploteos realizados de cada uno de los 8 canales representan la frecuencia de la señal en tiempo continuo para un mejor análisis.

Existe opacidad en el mapa de color en las 8 ondas y se iluminan a medida que el usuario realice mayor actividad cerebral y las señales se vuelvan más fuertes. 

* Channel 2: En el “channel 2” se analiza la zona frontopolar más cercana al hemisferio derecho. Se puede analizar como inicialmente (en estado de total relajación con los ojos cerrados) no presenta alguna fluctuación en el cambio de señal repentino. Al analizar el periodo de tiempo pasados los 20 segundos, en donde se le pidió a nuestra compañera realizar actividades como abrir y cerrar los ojos, se observa una alteración en la señal en esta zona. La interpretación de esta señal es registro del esfuerzo de la zona muscular, al realizar la acción de abrir y cerrar los ojos, o neurológico. [10]
* Channel 1,3,4,7: El “channel” 3 no presenta una señal definida. No se pudo obtener un registro de información correcto. La causa más probable es el mal ajuste del tornillo, lo que ocasionó un mal contacto con la zona analizada. Otra posible causa es la interferencia que representa un gran porcentaje de cabello en la toma de señales. Es importante mencionar que una de las posibles interferencias en la toma de datos es el movimiento de la mandíbula al hablar (cuando el usuario contestó las preguntas realizadas en las pruebas); además, al apretar la mandíbula se genera un artefacto EMG enorme en los 8 canales, aumentando la amplitud y fuerza de las ondas. Esto se pudo haber evidenciado en los canales 3 y 4, ya que los electrodos correspondientes a estos canales se encuentran más cerca a los músculos que producen ese artefacto EMG de la mandibula.. 
* Chanel 5,6,8: Cuando se cierra los ojos se ve un pico en el gráfico fft, aproximadamente a 10Hz, principalmente en los canales 5, 6 y 8 ya que están sobre la corteza visual del usuario. Estas son ondas cerebrales alfa.  [11]

#### > Señales ploteadas:
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Channel 2</p>
    <img src="https://user-images.githubusercontent.com/43499263/233427935-4c8c6ccc-d37d-4a99-bc2a-b8da4793771c.png" alt="Snow" style="width:90%">
  </div></th>
            <th><div class="column">
                <p>Channel 3</p>
    <img src="https://user-images.githubusercontent.com/43499263/233428205-832c5775-3de0-4183-b2c1-720fd07c9e40.png" alt="Snow" style="width:90%"></th>
    
<th><div class="column">
                <p>Channel 5</p>
    <img src="https://user-images.githubusercontent.com/43499263/233428390-14f7cc72-dd7c-4888-804c-13e32519bdbd.png" alt="Forest" style="width:90%"></th>
    
<th><div class="column">
                <p>Channel 6</p>
    <img src="https://user-images.githubusercontent.com/43499263/233428668-8c090b5b-07f0-44c0-ba02-bd87455fe16e.png" alt="Forest" style="width:90%"></th>
    
<th><div class="column">
                <p>Channel 8</p>
    <img src="https://user-images.githubusercontent.com/43499263/233428795-284f6e3c-52ff-422e-b298-8baedd891939.png" alt="Forest" style="width:90%"></th>    
  </table>
 </p>
 
##### Link del Código BITalino: https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/Informe_N%C2%B04/EEG_analisis%20(1).ipynb
##### Link del Código OpenBCI: https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/Informe_N%C2%B04/EEG_analisisOpenBCI.ipynb
##### Regresar a la Carpeta del Laboratorio 4: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes/Informe_N%C2%B04
## Referencias 
- [1] “Electroencefalografía (EEG) - Mayo Clinic,” Mayoclinic.org, 2022. [Online]. Available: https://www.mayoclinic.org/es-es/tests-procedures/eeg/about/pac-20393875. [Accessed: Apr. 19, 2023] ‌
- [2]M. Proença and K. Mrotzeck |, "BITalino (r)evolution Home Guide," Feb. 15, 2021, BITalino (r)evolution Lab Guide EXPERIMENTAL GUIDES TO MEET & LEARN YOUR BIOSIGNALS, Lisboa, Portugal, HOME-GUIDE #3 ELECTROENCEPHALOGRAPHY (EEG).
- [3] Fisiología de la Actividad Eléctrica del Cerebro (no date). Available at:
https://fisiologia.facmed.unam.mx/wp-content/uploads/2019/09/UTI-pr%C3%A1ctica-7-a.-Ele
ctroencefalograma.pdf (Accessed: April 20, 2023).
- [4] El, “Localización de electrodos del EEG: Layout Fijo vs. Variable | Bitbrain,”
Bitbrain, Apr. 30, 2020. https://www.bitbrain.com/es/blog/colocacion-electrodos-eeg
(accessed Apr. 20, 2023).
- [5]L. Morillo, “Acnweb.org,” Análisis visual del Electroencefalograma. [Online]. Available: https://www.acnweb.org/guia/g7cap17.pdf. [Accessed: 20-Apr-2023] 
- [6] Oshlumh, “OpenBCI: un escáner cerebral ‘open source’ – Oficina de Software y
Hardware Libre Universidad Miguel Hernández UMH,” Oshl.umh.es, 2013.
https://oshl.umh.es/2014/06/09/openbci-un-escaner-cerebral-open-source/
(accessed Apr. 20, 2023).
- [7] “Ultracortex ‘Mark IV’ EEG Headset,” OpenBCI Online Store, 2015.
https://shop.openbci.com/products/ultracortex-mark-iv (accessed Apr. 20, 2023).
- [8] “Ultracortex Mark IV | OpenBCI Documentation,” Openbci.com, Sep. 28, 2022.
https://docs.openbci.com/AddOns/Headwear/MarkIV/ (accessed Apr. 20, 2023).
- [9] “BITalino (r)evolution Lab Guide.” Available:
https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide3_EEG.p
df 
‌- [10] Conor Russomanno. (2015, 1 de noviembre). Ultracortex & OpenBCI GUI Demo by Conor Russomanno [Video]. YouTube. https://www.youtube.com/watch?v=agV1B2l-QLw
- [11] Urgidés Cárdenas, D. (2017). Implementación de un sistema BCI para el Análisis de un Comportamiento de Bioseñales Neurológicas [PARA OBTENER EL TÍTULO DE INGENIERO ELECTRÓNICO]. Universidad del Azuay.
