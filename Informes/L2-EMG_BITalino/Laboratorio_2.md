#  Informe de laboratorio
    
# Tabla de contenidos 
------------------------------------------------------------------------------------------------
- Objetivos del laboratorio
- Materiales
- OpenSignals
- Ploteo de señales en Python
- Archivo del codigo 
- Explicacion y resultados
---------------------------------------------------------------------------------------------------------------------------------------------------------------------    
 
## Objetivos del Laboratorio
- Adquirir señales biomédicas de EMG y ECG.
- Hacer una correcta configuración de BITalino. 
- Extraer la información de las señales EMG y ECG del software OpenSignals (r)evolution.
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

## Electromiografía
### ¿Qué es la técnica de electromiografía?
- Es una técnica de diagnóstico médico que evalúa la actividad eléctrica de los músculos y los nervios que la controlan
### Fundamento de la Electriomiografía
- Se basa en la medición de los biopotenciales musculares generados por la actividad muscular (contracción y relajación del músculo)
### Aplicaciones
- Lesiones musculares
- Detección de enfermedades neuromusculares
- Evaluación de la función muscular
## OpenSignals
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
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/conexion_1.jpg" alt="Forest" style="width:60%"></th>
    </table>
 </p>
 
### Ploteo de la señal usada en OpenSignals
 <p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal en reposo </p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos//reposo.jpg" alt="Snow" style="width:60%">
  </div></th>
            <th><div class="column">
                <p>Video </p>
                <p>Link: https://youtu.be/EahUPmu1-Ps </p>
    </table>
 </p>
        
 <p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal a un esfuerzo moderado </p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos//esfuerzo_medio.jpg" alt="Snow" style="width:60%">
  </div></th>
            <th><div class="column">
                <p>Video </p>
                <p> Link: https://youtu.be/bheNZn3Xyd0 </p>
    </table>
 </p>
 
 <p>
    <table>
        <tr>
            <th><div class="column">
                <p>Señal a un esfuerzo fuerte </p>
    <img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/esfuerzo_fuerte.jpg" alt="Snow" style="width:60%">
  </div></th>
            <th><div class="column">
                <p>Video </p>
                <p> Link: https://youtu.be/bheNZn3Xyd0 </p>
    </table>
 </p>

## Ploteo de señales en Python

<p align="center">
  <img width="500" height="600" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/muestras_amplitud.jpg">
</p>

<p align="center">
  <img width="500" height="600" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/muestras_tiempo.jpg">
</p>


<p align="center">
  <img width="500" height="600" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/ploteo_FFT.jpg">
</p>


<p align="center">
  <img width="500" height="600" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/musculo_reposo.jpg">
</p>

<p align="center">
  <img width="500" height="600" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/musculo_activo.jpg">
</p>

## Explicación y resumen del procedimiento y resultados:
Se realizó una prueba experimental correspondiente a la recolección y evaluación del movimiento del grupo muscular de los bíceps con el dispositivo BitAlino a través de tres electrodos. Este experimento hace referencia a pruebas electromiográficas. De acuerdo a los resultados del ploteo en  "OpenSignals" se puede concluir lo siguiente:
- Se muestra una señal en reposo donde la activación de los músculos es nula y las fibras musculares están en reposo. La información que se visualiza puede incluir ruido propio de fuentes de error como la conexión de los electrodos de manera incorrecta.
- Luego, empieza el momento de activación muscular donde se realiza el movimiento de flexión de bíceps. La gráfica muestra un aumento en la amplitud lo cual indica que la fuerza muscular se está incrementando.
                                                                                                                     
        
