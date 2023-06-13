# *Informe de Laboratorio 3*
 ----------------------------------------------------------------------------------------
## Tabla de contenidos 
------------------------------------------------------------------------------------------------
- [Objetivos del laboratorio](#Objetivos-del-Laboratorio)
- [Materiales](#Materiales-utilizados)
- [Electrocardiografía](#Electrocardiografía)
- [Actividad del laboratorio](#Actividad-del-laboratorio)
   * [Conexiones Usadas](#Conexiones-usadas)
   * [Señales Generadas](#Estado-Basal)
   * [Interpretación De Señales](#Interpretación-de-la-señal) 
- [Referencias](#Referencias)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Objetivos del Laboratorio
- Adquirir señales biomédicas de EMG y ECG.
- Hacer una correcta configuración de BITalino. 
- Extraer la información de las señales EMG y ECG del software OpenSignals (r)evolution.
---------------------------------------------------------------------------------------------------------------
## Materiales utilizados
<p>
    <table>
        <tr>
            <th>1 cable de 2 hilos</th>
            <th>1 cable de 3 hilos</th>
            <th>5 electrodos</th>
            <th>1 bateria</th>
            <th>1 BITalino
    </table>
        </p>
<p align="center">
  <img width="200" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Materiales-ISB.jpeg">
</p>

## Electrocardiografía 
<p align="center">
  <img width="300" height="200" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/EKG_Complex_Signals.jpeg">
</p>


 ### _¿Qué representa un ECG?_ 

Un ECG representa un registro de la actividad eléctrica del corazón. Es una técnica de diagnóstico no invasiva que tiene un impacto clínico en la detección e investigación de la gravedad de enfermedades cardiovasculares.

### _¿Cuándo se necesita el uso de un ECG?_
Será necesario realizar a un paciente si es que este presenta dolor torácico, disnea o mareo, si presenta un episodio de desvanecimiento. También para pacientes que hayan tenido un accidente isquémico transitorio (AIT), que lo más probable es que se deba a una arritmia. Es importante recalcar que los síntomas que presente el paciente guiarán la interpretación del ECG

### _Derivaciones_
Se tienen 12 derivaciones. Seis derivaciones estándar y seis derivaciones precordiales
<p align="center">
  <img width="400" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ECG-DerivacionesPrec.jpeg">
</p>

### _Uso del BITalino_
El Bitalino presenta un sensor de ECG que permite captar las señales eléctricas, y con el uso de OpenSignals se puede generar una señal simulada de un dispositivo ECG.
Los dos electrodos de medición (IN +/-) son colocados a las clavículas y el electrodo de referencia en la cresta ilíaca para recibir la señal.
<p align="center">
  <img width="500" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ElectrodosClavi.jpeg">
</p>

### _Aplicaciones del sensor_
 * Ritmo cardíaco y variabilidad del ritmo cardíaco
 * Interacción Persona-Ordenador
 * Biometría
 * Computación afectiva
 * Estudios de fisiología
 * Psicofisiología
 * Biorretroalimentación
 * Prototipado de dispositivos biomédicos

*Datasheet* : [revolution-ecg-sensor-datasheet-revb-1.pdf](https://github.com/Harold01082001/Proyecto_IntroSe-ales/files/11216901/revolution-ecg-sensor-datasheet-revb-1.pdf)

## Actividad del laboratorio
Para realizar las pruebas del sensor ECG BITalino hemos usado la configuración de la derivación I de Einthoven, posicionando los electrodos en la clavícula y la cresta ilíaca. El electrodo positivo (rojo) se ubicó en la clavícula izquierda (LA) y el electrodo negativo (negro) en la clavícula derecha (RA). La referencia (REF) en blanco se situó en la cresta ilíaca. Por otro lado, para la toma de la data planteamos 3 fases, en estado basal, respiración profunda, en actividad física.


### Conexiones usadas
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>BITalino-Cables</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/conexion_2.jpg" alt="Snow" style="width:40%">
  </div></th>
            <th><div class="column">
                <p>Electrodo-Cuerpo </p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/conexion_usada3.jpg" alt="Forest" style="width:50%"></th>
    </table>
 </p>


### Estado Basal
En reposo, la señal del ECG mostrará una forma de onda regular que representa la actividad eléctrica del corazón en un estado relajado. Una señal de ECG normal en reposo incluirá ondas P, complejos QRS y ondas T. La duración de la toma de datos demoro 30s. 

<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/reposo_lab3.jpg" alt="Snow" style="width:70%">
  </div></th>
            <th><div class="column">
                <p>Video de la toma de la señal </p>
    <video src="https://user-images.githubusercontent.com/128879214/231529169-1e2769da-6557-4a9b-a6de-a2d0fa10de68.mp4" alt="Forest" ></video></th>
    </table>
 </p>

### Respiración profunda
El contener la respiración puede reducir temporalmente el flujo sanguíneo y reducir la cantidad de oxígeno en su cuerpo. Esto afecta la actividad eléctrica del corazón y en algunos casos provoca cambios en la curva de ECG. La segunda medición fue mientras se generaba una variación en la respiración, se paso a aguantar la respiración 5s y luego descansar, se repetio esta secuencia 3 veces. 

<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/reposo2_lab3.jpg" alt="Snow" style="width:70%">
  </div></th>
            <th><div class="column">
                <p>Sin Respirar 5x3</p>
    <video src="https://user-images.githubusercontent.com/128879214/231534693-41d55206-a4ff-43bc-b8ae-43d4314a4088.mp4" alt="Forest" ></video></th>
    <th><div class="column">
                <p>Reposo post respirar</p>
    <video src="https://user-images.githubusercontent.com/128879214/231530496-ca342337-8057-4f18-9753-c24de1426210.mp4" alt="Forest" ></video></th>
  </table>
 </p>


### Actividad física
El movimiento puede afectar la señal de la forma de onda del ECG porque el movimiento del cuerpo puede causar perturbaciones eléctricas y artefactos que pueden afectar la calidad de la señal del ECG. Por lo tanto, para obtener resultados precisos, es muy importante evitar el movimiento durante el ECG.  La última medición fue luego de realizar actividad física por 5 min.
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal en actividad fisica</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/actividad_fisica.jpg" alt="Snow" style="width:70%">
  </div></th>
            <th><div class="column">
                <p>Video de la toma de la señal </p>
    <video src="https://user-images.githubusercontent.com/128879214/231533657-c0c60397-d8da-4fe7-9da4-f0da0cca7a9e.mp4" alt="Forest" ></video></th>
    </table>
 </p>

## Interpretación de las señales
Antes de la actividad, en reposo se muestra la señal del ectrocardiograma estable de acuerdo a la primera figura (ploteo) del ECG. En este caso la amplitud se aproxima a 70 y se utilizará como referencia para poder interpretar las fluctuaciones presentadas a la hora de realizar actividad física. La frecuencia con la cual se repite la onda completa se ve constante. Por otro lado, cuando deja de respirar aumenta la frecuencia y ya no es constante, así como no es estable. En el caso del movimiento, se aproxima la amplitud a 100. Es coherente indicar que en el movimiento la cantidad de información eléctrica que transmite el corazón sea mayor por el esfuerzo que realiza para generar una contracción y eyectar la cantidad de sangre suficiente y necesaria a todo el cuerpo.
<p>
    <table>
        <tr>
            <th><div class="column">
                <p>ECG en reposo</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ECG_REPOSO.jpg" alt="Snow" style="width:70%">
  </div></th>
            <th><div class="column">
                <p>ECG sin respirar</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ECG_SIN_RESPIRAR.jpg" alt="Forest" style="width:70%"></th>
    
<th><div class="column">
                <p>ECG segundo reposo</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ECG_SEGUNDO_REPOSO.jpg" alt="Forest" style="width:70%"></th>
    
<th><div class="column">
                <p>ECG movimiento</p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ECG_MOVIMIENTO.jpg" alt="Forest" style="width:70%"></th>
    

  </table>
 </p>

## Referencias 
- [1] Electrocardiogram - StatPearls - NCBI Bookshelf. (s.f.). National Center for Biotechnology Information. https://www.ncbi.nlm.nih.gov/books/NBK549803/
- [2] “ECG Fácil - John Hampton - Google Libros”. https://books.google.es/books?hl=es&lr=&id=7cnSDwAAQBAJ&oi=fnd&pg=PP1&dq=gu%C3%ADa+de+uso+del+ecg&ots=FcLWoBIR_x&sig=qaae6BJpafJvZhqRvAW9-qMFDqI#v=onepage&q=gu%C3%ADa%20de%20uso%20del%20ecg&f=false (consultado el 29 de marzo de 2023).
- [3] Sinus Rhythm - Normal Function of the Heart - Cardiology Teaching Package - Practice Learning - Division of Nursing - The University of Nottingham. (s.f.). University of Nottingham. https://www.nottingham.ac.uk/nursing/practice/resources/cardiology/function/sinus_rythm.php#:~:text=Sinus%20rhythm%20is%20the%20name,3%20distinct%20waves%20on%20ECG
- [4] Chamley, R. R., Holdsworth, D. A., Rajappan, K., & Nicol, E. D. (2019). ECG interpretation. European Heart Journal, 40(32), 2663–2666. https://doi.org/10.1093/eurheartj/ehz559
- [5] Nova Biosignals. (2015, 5 de febrero). BITalino Tutorial: How to do an ECG [Video]. YouTube. https://www.youtube.com/watch?v=Usiiofm-khY
