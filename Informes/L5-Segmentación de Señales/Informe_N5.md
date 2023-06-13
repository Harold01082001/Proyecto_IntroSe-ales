# *Informe de Laboratorio 5*
 ----------------------------------------------------------------------------------------
## Tabla de contenidos 
------------------------------------------------------------------------------------------------
- [Objetivos del laboratorio](#Objetivos-del-Laboratorio)
- [Tratamiento de señales](#Tratamiento-de-señales)
   * [Señales de interés](#Señales-de-interés)
   * [Sistemas](#Sistemas)
- [Transformadas y aplicaciones](#Transformadas-y-aplicaciones)
- [Referencias](#Referencias)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Objetivos del Laboratorio
- Crear un dataset con toda la información de la señal de ECG que contenga:
  * Base : Data observada en estado de reposo
  * Post_ejercicio : Data observada despues de ejercicio 

---------------------------------------------------------------------------------------------------------------
## Tratamiento de señales
El procesamiento de señales permite transformar datos a una manera que se puedan optimizar, corregir o clasificar de una manera más directa y optimizada [1].

<p align="center">
  <img width="500" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/dsp1.jpg">
</p>

El procesamiento de señales comienza en el dominio analógico; luego se pasa al primer paso que es la digitalización, para esto se utiliza un ADC. El ADC nos pemite convertir señales analógicas a digitales, para esto primero se muestrea la señal, luego se cuantifica con respecto a la resolución deseada ,para finalmente establecer sus valores binarios y se pueda enviar al sistema [2]. 

La tasa de muestro que utilizamos en un ADC se mide en "muestras por segundo" lo cual se relaciona a la velocidad del sistema. Una forma fácil de explicar esto es viendo que por cada segundo cuantas muestras se van a utilizar ,lo que significa que mientras más muestras por segundo se consideren la tasa de frecuencia va a disminuir esto por la siguiente relación [2]: 

<p align="center">
  <img width="500" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/fs.jpg">
</p>

Después de la conversación ADC se pasa al procesamiento de la señal digital para lo cual la señal pasamos a representar en su dominio de tiempo, donde utilizamos la Transformada de Fourier. Luego de esto la señal podrá cuantificarse y entrar a filtros. Por último está el paso de volver la señal a analógica, para lo cual utilizamos un DAC. Los DAC son conversores capaces de transformar una señal digital (código binario) en una señal analógica que puede ser una tensión, corriente o carga eléctrica. Generalmente los datos sítiales son una secuencia de impulsos de tiempo finitos que son procesados y convertidos en una señal analógica física continua. Una de las principales aplicaciones de un DAC es para reducir el ruido en una señal, como por ejemplo una fuente de sonido se puede eliminar el ruido de fondo si se escucha [3].


### _Señales de interés_ 
Las señales son una forma de transmitir información, como lo son las imagnes, sonidos, o gestos. Existen tres formas de clasificar una señal: en tiempo continuo y discreto, en analógico y digital ,y periódica y aperiódica. Para su procesamiento estas deben digitalizarse donde se convierten en una secuencia de valores finitos; entre las señales de conversión de interes tenemos las siguientes [4]:

<p align="center">
  <img width="500" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/señal.jpg">
</p>

### _Sistemas_
En el procesamiento de señales desde la perspectiva de una computadora es un dispositivo que toma como entrada una señal binaria y devuelve como salida en binario más señales [5].

<p align="center">
  <img width="500" height="300" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/system.jpg">
</p> 

## Transformadas y aplicaciones

### Transformada de Laplace: 
* Representación: 
  <p align="center">
    <img width="250" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/TransL.jpg">
  </p>
  
* Utilidad en Señales [6]:
 La transformada de Laplace caracteriza las señales del dominio en el tiempo continui en un dominio de frecuencia complejo. Además, representa los sistemas analógicos mediante la función de transferencia.
 

### Transformada de Fourier:
* Representación:
 <p align="center">
    <img width="300" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/TransF.jpg">
  </p>
  
* Utilidad en Señales [7]:
  La transformada de Fourier transforma una señal muestrada en tiempo o espacio con la misma señal muestrada en frecuencia temporal o espacial. 
  La apicación en el procesamiento de señales se basa en revelar características de una señales, componentes de frecuencia.
  
### Transformada Z:
* Representación:
 <p align="center">
    <img width="300" height="100" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/TZ.jpg">
  </p> 
  
* Utilidad en Señales [8]:
 La transformada Z es una generalización de la transformada de Fourier. En procesamiento de señales, la transformada Z convierte una señal real/compleja (dominio discreto) en una representación en el dominio de la frecuencia.

#### _Señales generadas_: https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/Informe_N5/Entregable_Semana_5_SegmentacionSe%C3%B1ales.ipynb
#### _Carpeta del laboratorio 5_: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes/Informe_N5

## Referencias 
- [1]“What is Signal Processing?,” Data Acquisition | Test and Measurement Solutions, Mar. 14, 2023. [Online]. Available: https://dewesoft.com/blog/what-is-signal-processing. [Accessed: Apr. 26, 2023]
- [2]M. Gudino, “Analog-to-Digital Converters Basics,” Arrow.com, Apr. 17, 2018. [Online]. Available: https://www.arrow.com/en/research-and-events/articles/engineering-resource-basics-of-analog-to-digital-converters#:~:text=ADCs%20follow%20a%20sequence%20when,its%20sampling%20rate%20and%20resolution.. [Accessed: Apr. 26, 2023]
- [3]Daniel Perez Fernandez, “▷ ¿Qué es un DAC? Todo lo que debes saber,” Tecnonucleous, Aug. 28, 2018. [Online]. Available: https://tecnonucleous.com/2018/08/28/que-es-un-dac/. [Accessed: Apr. 26, 2023]
- [4]“3.1 Digital Signal Processing,” Ircam.fr, 2023. [Online]. Available: http://recherche.ircam.fr/anasyn/schwarz/da/specenv/3_1Digital_Signal_Processin.html. [Accessed: Apr. 26, 2023]
- [5]Stein (2000) Digital Signal Processing a computer science perspective. New York: John Wiley. 
- [6] Laplace Transform. In Signals and Systems: Principles and Applications (pp. 513-617). Cambridge: Cambridge University Press. doi:10.1017/CBO9781316536483.008
- [7] Transformadas de Fourier- MATLAB & Simulink- MathWorks América Latina. (s.f.). MathWorks - Creadores de MATLAB y Simulink - MATLAB y Simulink - MATLAB & Simulink. https://la.mathworks.com/help/matlab/math/fourier-transforms.html
- [8] Señales y sistemas: principios y aplicaciones. Cambridge: Cambridge University Press. doi:10.1017/CBO9781316536483
‌
