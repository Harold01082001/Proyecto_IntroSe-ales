# *Tratamiento de señal EMG*
 ----------------------------------------------------------------------------------------
## Tabla de contenidos 
------------------------------------------------------------------------------------------------
- [Procedimiento](#Procedimiento)
- [EMG Breve Explicación](#EMG-Breve-Explicación)
- [Señales generadas EMG](#Señales-generadas-EMG)
- [Técnicas Para el Procesamiento](#Técnicas-Para-el-Procesamiento)
- [Referencias](#Referencias)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Procedimiento
* 1. Filtrado de la señal EMG.
* 2. Rectificación de la señal EMG.
* 3. Suavizado de la señal EMG.
* 4. Extracción de características de la señal EMG.
* 5. Análisis temporal y frecuencial de la señal EMG.

---------------------------------------------------------------------------------------------------------------
## EMG Breve Explicación
La electromiografía es una técnica de diagnóstico médico que se utiliza para evaluar la actividad eléctrica de los músculos mediante la detección de los biopotenciales producidos por las células musculares (contracción y relajación).[1]

<p align="center">
  <img width="400" height="350" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/085ad49f-8c30-473f-a499-d2d91bb431d1">
</p>

La técnica EMG se utiliza en diferentes aplicaciones, como la evaluación de lesiones musculares, la detección de enfermedades neuromusculares y la evaluación de la función muscular. La técnica también se utiliza en la investigación para estudiar el comportamiento de los músculos y la actividad muscular en diferentes situaciones, como el ejercicio y el movimiento. [2]


### Señales generadas EMG
<p align="center">
  <img width="700" height="250" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/assets/43499263/6212c3fd-0a9e-427e-9d97-4b98f64d606a">
</p>
 
### Técnicas Para el Procesamiento
 * Amplificación: Las magnitudes bioeléctricas al ser muy pequeñas se necesita amplificar la señal entre 50 a 250 000 veces. Las señales amplificadas son de entre 1 a 10V 
 * Eliminación del ruido: Ruido técnico o biológico. Los amplificadores diferenciales pueden neutralizar buena parte del ruido.
 * Filtrado: Uso de filtros para eliminar frecuencias superiores o inferiores a las propias de la señal fisiológica. 
    - Frecuencias inferiores a 2-5 Hz: Debido a fluctuaciones lentas por movimiento de agujas.
    - Frecuencias superiores a 10 kHz: Oscilaciones rápidas de la señal de origen técnico.
    - Osilación de la señal a 60 Hz: Debido a la corriente alterna de la red eléctrica
    * Recomendación: Filtro Notch
 * Digitalización: Los sistemas analógicos operan con la señal como una variación continua de voltaje. La digitalización, ejecutada en conversores analógico-digitales, consiste en la obtención de medidas (muestras) a intervalos regulares de tiempo. Debe respetarse el teorema Nyquist para la frecuencia de muestreo [3]

#### Link para descargar el código (zip): https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/L8%20-%20Tratamiento%20de%20se%C3%B1ales%20EMG%20%2B%20EEG/Tratamiento%20de%20se%C3%B1al%20EMG/C%C3%B3digo_EMG.zip
#### Regresar a la carpeta del Informe 8: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes/L8%20-%20Tratamiento%20de%20se%C3%B1ales%20EMG%20%2B%20EEG
#### Regresar a la carpeta de informes: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes


## Referencias 
- [1]"Electromiografía - Mayo Clinic". Mayo Clinic - Mayo Clinic. https://www.mayoclinic.org/es-es/tests-procedures/emg/about/pac-20393913 (accedido el 31 de mayo de 2023).
- [2] "ElectromiografÃ­a y estudios de conducciÃ³n nerviosa: Prueba de laboratorio de MedlinePlus". MedlinePlus - Health Information from the National Library of Medicine. https://medlineplus.gov/spanish/pruebas-de-laboratorio/electromiografia-y-estudios-de-conduccion-nerviosa/ (accedido el 31 de mayo de 2023).
- [3] Gila, L., Malanda, A., Rodríguez Carreño, I., Rodríguez Falces, J., & Navallas, J.. (2009). Métodos de procesamiento y análisis de señales electromiográficas. Anales del Sistema Sanitario de Navarra, 32(Supl. 3), 27-43. Recuperado en 31 de mayo de 2023, de http://scielo.isciii.es/scielo.php?script=sci_arttext&pid=S1137-66272009000600003&lng=es&tlng=es.


‌
‌
‌

‌


‌
