# *Informe de Laboratorio 6*
 ----------------------------------------------------------------------------------------
## Tabla de contenidos 
------------------------------------------------------------------------------------------------
- [Objetivos del laboratorio](#Objetivos-del-Laboratorio)
- [Introducción a Filtros](#Introducción-a-Filtros)
- [Filtros FIR](#Filtros-FIR)
   * [La ventana Hanning](#La-ventana-Hanning)
   * [La ventana Hamming](#La-ventana-Hamming)
   * [La ventana blackman](#La-ventana-blackman)
   * [La ventana Bartlett](#La-ventana-Bartlett)
   * [La ventana Rectangular](#La-ventana-Rectangular)
- [Filtros IIR](#Filtros-IIR)
- [Aplicación de los filtros](#Aplicación-de-los-filtros)
- [Referencias](#Referencias)
---------------------------------------------------------------------------------------------------------------
## Objetivos del Laboratorio
- Usando dataset de ECG creada del laboratorio anterior, deben filtrar las frecuencias altas de dichas
señales que corresponden a ruido, dichos filtros deben ser los más óptimos.
  - Usar Filtros IIR y Filtros FIR

---------------------------------------------------------------------------------------------------------------
## Introducción a Filtros 
<p align="center">
  <img width="700" height="200" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/FiltorsFI.jpg">
</p>

* (a)Filtro FIR: Respuesta impunsional finita. Se retarta una copia de la señal del entrada y se combina con la nueva señal de entrada [1]. 
* (b)Filtro IIR: Respuesta impunsional infinita. Se retarda una copia de la señal de salida y se combina con la nueva señal de entrada [1].

## Filtros FIR 
Este uno de los filtros digitales más utilizado en el procesamiento de señales digitales (DSP). FIR es la abreviatura de una "Respuesta de impulso finito"; es decir, es un filtro que da como respuesta un peridodo finito a una señal de impulso [2]. 

Con respecto a los filtros FIR para su procesamiento se usa el método de ventanas, el cual nos permite seccionar la respuesta a un filtro ideal. Entre los mpétodos de ventana que se usan con los filtros FIR estan:
* Hanning
* Hamming
* Bartlett
* Rectangular
* Blackman 

### La ventana Hanning

Es conocida como la Campana de Coseno ya que tiene la forma de un ciclo de onda conoseonoidal, este método usa la transformada de Fourier para su filtrado y se define de la siguiente manera [3]:
<p align="center">
  <img width="600" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/hann.png">
</p>
Este tipo de ventana nos permite forzar las extremidades a un valor cercano a cero , mientras que distoriciona la señal de entrada a la forma de una onda [4]. 

### La ventana Hamming

Este tipo de ventana usa para su formado un coseno levado con puntos finales distintos de cero y se define de la siguiente manera [5]:
<p align="center">
  <img width="600" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/hamm.png">
</p>
Se usa este método más que todo para reducir las discontinuidades al principio y al final de la señal medida. 

### La ventana blackman

Este tipo de ventana tiene una forma cónica que se forma por el uso de una seña de cosenos que se define de la siguiente manera [6]:
<p align="center">
  <img width="600" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/blac.png">
</p>
Este método se diseño con el fin de eliminar los lóbulos laterales terceros y cuartos; sin embargo, mantiene una discontinuidad en los límites. Esta ventana es conocida como la ventana más "exacta", aunque no elimine los lóbulos laterales si no las atenua. 


### La ventana Bartlett

Este tipo de ventana difiere en su forma más que las anteriores, ya que es muy parecida a una forma triangular, en específico, esta definida como el producto de dos funciones sinc de la siguiente manera [7]:
<p align="center">
  <img width="600" height="400" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/barle.png">
</p>
Su forma de diseño le ayuda más que todo a procesar señales sin la misma cantidad de ondulaciones en el dominio en comparación con los anteriores casos. Por otro lado, otra diferencia es que las señales iniciales y finales no las elimina , si no las "suaviza".

### La ventana Rectangular

Por útlimo esta la ventana rectangular, este tipo de ventana posee solo dos valores (0 o 1) para intervalos determinados, y se ve de la siguiente manera [8]:
<p align="center">
  <img width="500" height="200" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/recta.png">
</p>
Como se puede ver en la imagen anterior, la amplitud es constante para todo el intervalo de 1, por lo que la señal no se ve afectada. Sin embargo, cuando el intervalo cambia a 0 la  ventana suprime los valores. 

## Filtros IIR 
Como se visualiza en la imagen presentada en la introducción, en un filtro IIR se presenta una efecto de recursividad. El efecto de recursividad se basa en la conexión entre la deñal salida y la señal de entrada como un efecto "feedback"; generando filtros con respuestas más complejas y con menor cantidad de datos. 


#### Filtros Butterworth: 
 Produce la respuesta más plana posible hasta la frecuencia de corte, logrando que la salida se mantenga lo más constante hasta la frecuencia de corte, posteriormente decayendo a razón de 20n dB por década (n=número de polos del filtro) [9]
 Fundamento de diseño: La respuesta en magnitud del filtro es máximamente plana en la banda pasante y en la no pasante. Debe cumplir: (2N-1) primera derivadas de H(w) sean 0, para  w=0 y w -> infinito
 Función de transferencia: 
 <p align="center">
 <img width="400" height="150" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Butt.jpg">
 </p>
 [10]
 Explicación de la fórmula:

 * wc: Frecuencia de corte
 * N: Orden del filtro
 * Se visualiza que únicamente posee polos
 
 #### Filtros Bessel
 Diseñados para poseer una fase lineal en las bandas pasantes, por lo cual no se distorsionan las señales; por el contrario tienen mayor zona de transición entre las bandas pasantes y no pasantes. Al transformarse a digital pierden su propiedad de fase lineal y presentan menor pendiente. [9][11]
 Funcion de transferencia:
  <p align="center">
 <img width="650" height="250" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Bessel.jpg">
 </p>
 
 #### Filtros Chebyshev
 Caída de respuesta en frecuencia más pronunciada debido que permite el rizado en alguna de sus bandas, ya sea de paso o de rechazo. La diferencia más notoria con los otros dos filtros analizados es su distribución de polos sobre una elipse (no una circunferencia) y los ceros sobre el eje imaginario. Se consideran la mejor aproximación a un filtro ideal, debido que la respuesta en la región de corte es más rectangular y en la banda de supresión poseen un índice de descenso más abrupto.
 <p align="center"> [9] [10] [11]
 <img width="400" height="150" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Che.jpg">
 </p>
 
 #### Filtros Elipticos 
  Se consigue estrechar la zona de transición generando un rizado constante en ambas bandas. Este tipo de filtros presenta fase menos lineal, en general en el extremo de la banda pasante [12]
  <p align="center">
 <img width="650" height="250" src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Elip.jpg">
 </p>

## Aplicación de los filtros

<table>
    <caption>Análisis</caption>
    <tr>
        <th scope="col">Situación </th>
        <th scope="col">Señal original</th>
        <th scope="col">Señal con el filtro FIR</th>
        <th scope="col">Señal con el filtro IRR</th>
    </tr>
    <tr>
        <th scope="row">EEC en reposo 1</th>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/reposo1.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/FILTRO1.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Reposo1.jpg" alt="Forest" style="width:90%"></td>
    </tr>
    <tr>
        <th scope="row">EEC sin respirar</th>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/norespirar.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/FILTRO2.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/SinRespirar.jpg" alt="Forest" style="width:90%"></td>
    </tr>
    <tr>
        <th scope="row">EEC en reposo 2</th>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/reposo2.png" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/FILTRO3.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Reposo2.jpg" alt="Forest" style="width:90%"></td>
    </tr>
 
 <tr>
        <th scope="row">EEC en actividad física </th>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/movimiento.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/FILTRO4.jpeg" alt="Forest" style="width:90%"></td>
        <td><img src="https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Fotos/Movimiento.jpg" alt="Forest" style="width:90%"></td>
    </tr>
</table>
 
 ### Elección de la ventana (FIR) y del tipo de filtro (IRR)
#### FIR:
En el caso del filtro FIR, se escogió el filtro **Blackman** principalmente por la atenuación que presenta. En general, la atenuación que proporciona este filtro es bastante significativa en los laterales, por lo que su capacidad para minimizar el ruido y suavizar las señales es bastante alta. Esto sucede principalmente por la forma que posee la ventana Blackman, lo cual resulta útil para la señal representada. Adicionalmente, es de simple implementación y eficiente computacionalmente [13]. Por otro lado, es importante mencionar que muestra una muy buena respuesta en frecuencia y se pueden obtener los resultados esperados mediante la variación del tamaño de la ventana [14]

#### IIR:
Para desarrollar el filtro de IIR se escogió diseñar el tipo de filtro **Butterworth** debido a que este filtro es suave y la respuesta de la frecuencia decrece monótonamente en la región de transición.
Asimismo, los filtros Butterworth son fáciles de diseñar ya que los valores resultantes de los componentes son más prácticos que la mayoría de los otros tipos y, en estos filtros, las variaciones de los componentes son menos críticas. El filtro de
Butterworth es el único filtro que mantiene su forma para órdenes mayores (sólo con una caída de más pendiente a partir de la frecuencia de corte) y necesita un mayor orden para los mismos requerimientos en comparación con otros. [10]

 ### Comentario de las señales filtradas
 De manera general se puede observar que las señales filtradas por FIR como con IIR, presentan una disminución en el ruido y la reducción de ciertas interferencias; además, al pasar por el filtro, hay una disminución en la amplitud de algunos componentes no deseados o que están fuera del rango de interés. 

Se pudo observar en las gráficas que el filtro FIR fue más efectivo que el filtro IIR, ya que los filtros FIR son inherentemente estables, lo que los hace ideales para aplicaciones de filtrado pasabanda y supresión de banda; mientras que, los filtros IIR son más eficientes en cuanto a procesamiento de señales pero son menos estables. Estos son usados principalmente en aplicaciones de filtrado de paso bajo y suavizado. [15]

### Liink de los archivos:
* Regresar a la carpeta del laboratorio: https://github.com/Harold01082001/Proyecto_IntroSe-ales/tree/main/Informes/Laboratorio%206
* Diseño del Filtro FIR (código): https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/Laboratorio%206/FIR_dise%C3%B1o_G7_final.ipynb
* Diseño del Fitro IIR (código): https://github.com/Harold01082001/Proyecto_IntroSe-ales/blob/main/Informes/Laboratorio%206/IIR_dise%C3%B1o_G7_final.ipynb

---------------------------------------------------------------------------------------------------------------

## Referencias 
* [1] Gómez, E. (2009). Introducción al filtrado digital.
* [2] T. Agarwal, “What is FIR Filter? - FIR Filters for Digital Signal Processing,” ElProCus - Electronic Projects for Engineering Students, Jul. 10, 2015. [Online]. Available: https://www.elprocus.com/fir-filter-for-digital-signal-processing/. [Accessed: May 03, 2023]
* [3] “numpy.hanning — NumPy v1.24 Manual,” Numpy.org, 2022. [Online]. Available: https://numpy.org/doc/stable/reference/generated/numpy.hanning.html. [Accessed: May 03, 2023]
* [4] “Comprender FFTs y Funciones Ventana,” Ni.com, 2023. [Online]. Available: https://www.ni.com/es-cr/shop/data-acquisition/measurement-fundamentals-main-page/analog-fundamentals/understanding-ffts-and-windowing.html. [Accessed: May 03, 2023]
* [5]“scipy.signal.windows.hamming — SciPy v1.10.1 Manual,” Scipy.org, 2023. [Online]. Available: https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.windows.hamming.html. [Accessed: May 03, 2023]
* [6] “scipy.signal.windows.blackman — SciPy v1.10.1 Manual,” Scipy.org, 2023. [Online]. Available: https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.windows.blackman.html. [Accessed: May 03, 2023]
* [7] “scipy.signal.windows.bartlett — SciPy v1.10.1 Manual,” Scipy.org, 2023. [Online]. Available: https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.windows.bartlett.html. [Accessed: May 03, 2023]
* [8] dfalvarado, “Efecto del enventanado en la obtención del espectro discreto de una señal,” Monografias.com, Apr. 18, 2005. [Online]. Available: https://www.monografias.com/trabajos20/enventanado/enventanado. [Accessed: May 03, 2023]
* [9] Universidad Nacional de Rosario. (2019). Dispositivos y Circuitos Electrónicos II -Notas de Clase – Filtros Activos (2a ed.).
‌* [10] Salas, P., & Campos, I. (2014). FILTROS NO LINEALES. Revista Académica de Investigación, Artículo 17.
* [11] Madrid, D. (2017). Implementación de Filtros Pasa Baja: Bessel y Chebyshev. Universidad Tecnológica Centroamericana.
* [12] Martínez, M., Gómez, L., Serrano, A., Vila, J., & Gómez, J. (2019). Revisión de los tipos de filtros analógicos más comunes. En FILTRADO DIGITAL (pp. 8–9).
* [13] “Filtros senoc-enventanado Filtros personalizados clase 11.” Available: https://www.eumus.edu.uy/eme/ensenanza/electivas/dsp/presentaciones/clase11.pdf
* [14] “FILTROS DIGITALES FILTROS FIR (Respuesta Impulsional Finita) - PDF Descargar libre,” Docplayer.es, 2016. https://docplayer.es/98398905-Filtros-digitales-filtros-fir-respuesta-impulsional-finita.html (accessed May 04, 2023).
* [15] Difference Between FIR Filter and IIR Filter (with Comparison chart) - Circuit Globe. (s.f.). Circuit Globe. https://circuitglobe.com/difference-between-fir-filter-and-iir-filter.html#Conclusion


