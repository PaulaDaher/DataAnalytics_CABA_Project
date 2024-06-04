
# <h1 align=left> PROYECTO DE DATA ANALYTICS PARA LA CIUDAD DE BUENOS AIRES</h1>
# <h3 align=left>**`PAULA DAHER`**</h3>

<p align="center">
<img src="Images\portada.png" height=200>
</p>

# <h3 align=left>**`DESCRIPCIÓN DEL PROYECTO`**</h3>


El `Observatorio de Movilidad y Seguridad Vial` (OMSV), centro de estudios que se encuentra bajo la órbita de la ***Secretaría de Transporte*** del Gobierno de la Ciudad Autónoma de Buenos Aires, preocupado por sus altísimas tasas de mortalidad en siniestros viales, me encomendó hacer un proyecto de análisis de datos sobre su base de datos de accidentes de tránsito en el periodo del 2016 al 2021, para poder descifrar tendencias y patrones, comprender el comportamiento vehicular en la ciudad y poder tomar medidas acertivas. 

[Observatorio de Movilidad y Seguridad Vial](https://buenosaires.gob.ar/movilidad/plan-de-seguridad-vial/observatorio-de-movilidad-y-seguridad-vial)

Como data analyst del proyecto, realicé las siguientes tareas:
- Limpieza y Preparación de Datos. Normalicé y transformé los datos para hacerlos compatibles y consistentes. (DATOS)
- Análisis de Datos. Apliqué técnicas estadísticas y algoritmos para explorar y entender los datos. (DATOS)
- Identifiqué patrones, tendencias y relaciones dentro de los datos. (INFORMACIÓN)
- Visualización de Datos: Creé un dashboard con gráficos, tablas y otros tipos de visualizaciones para representar los datos de manera comprensible. (INFORMACIÓN)
- Conclusiones: Interpreté los resultados del análisis y saqué algunas conclusiones para que los interesados puedan tomar medidas acertadas. (CONOCIMIENTO)


-----------------------------------------------------------------------------------------------------

# <h3 align=left>**`ESTRUCTURA DEL PROYECTO`**</h3>
- **Data:.csv** En el repositorio se encuentran los archivos .csv que se recibieron (DB_seed), los archivos con un ETL aplicado (_ETL) y los archivos csv complementarios que se utilizaron para darle más profundidad al EDA.
- **Notebooks:** 4 Jupyter notebooks para ETL y para el EDA, y otros dos anexos que complementan el EDA (ETL de bases de datos complementarias).
- **Dashboard.pbix:** Archivo powerBi con el dashboard interactivo
- **README.md:** Descripción y guía del proyecto.
 
-----------------------------------------------------------------------------------------------------

# <h3 align=left>**`TECNOLOGÍA UTILIZADA`**</h3>
- Python: Lenguaje de programación principal.
- Pandas: Manipulación y análisis de datos.
- NumPy: Soporte para arrays y operaciones matemáticas de alto rendimiento.
- Matplotlib y Seaborn: Creación de gráficos.
- Power BI: Herramienta de inteligencia empresarial para la visualización interactiva de datos y generación de informes.
- Jupyter Notebook: Entorno interactivo para escribir y ejecutar código Python, ideal para análisis de datos y visualización.


-----------------------------------------------------------------------------------------------------

# <h3 align=left>**`FUENTES DE DATOS`**</h3>
**Obligatorio:**

- [Buenos Aires Data](https://docs.google.com/spreadsheets/d/1nq00jGIZHQ1RLSET43zKnUsMsoFb-pBg/edit#gid=1625530738)
- [Diccionario de datos](https://docs.google.com/spreadsheets/d/1Op98U-Hh2a3Q7uuznAzdl4Bf8r8qPr4m/edit#gid=1771770012)

**Complementarios:**

- [Comunas de la Ciudad de Buenos Aires](https://data.buenosaires.gob.ar/dataset/comunas)
- [Permisos para eventos masivos en la Ciudad de Buenos Aires](https://data.buenosaires.gob.ar/dataset/permisos-eventos-masivos)
- [Locales bailables en la Ciudad de Buenos Aires](https://data.buenosaires.gob.ar/dataset/locales-bailables)


-----------------------------------------------------------------------------------------------------


# <h3 align=left>**`PASOS REALIZADOS`**</h3>
## Transformaciones de Datos:  
Realicé la lectura de los dataset en el formato correcto, como así también la limpieza y preprocesamiento de los datos de las bases sobre las cuales trabajé posteriormente. 
Eliminé columnas innecesarias, imputé valores nulos y analicé valores atípicos, entre otros procedimientos.  
Las transformaciones se encuentran asentadas en el notebook [ETL_PI2](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/ETL_PI2.ipynb)

## Análisis Exploratorio de Datos:
Realicé un análisis exploratorio de los datos para entender mejor las relaciones entre las variables, detectar comportamiento y patrones interesantes que nos sirvan para poder tomar futuras decisiones.
Realicé gráficos coherentes según la tipología de la variable, los cuales me fueron brindando información valiosa para entender los comportamientos.
Todo el proceso se puede observar en el siguiente notebook: [EDA_PI2](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/EDA_PI2.ipynb)

Fué escencial cruzar el dato más importante con el que contábamos (**cantidad de víctimas: 715 en 6 años sólo en CABA**) con distintos factores como el paso del tiempo, las comunas de la ciudad de Buenos Aires, y datos de víctimas y acusados.

**SINIESTROS Y EL TIEMPO**   

Mediante el análisis de los 6 años comprendidos en el dataset pude observar algunos comportamientos regulares y otros atípicos. 
Dentro de los comportamientos regulares puedo destacar que los meses con más víctimas fatales en la Ciudad de Buenos Aires resultan ser los **últimos meses del año**, y dentro de los atípicos se puede ver que **en el año 2020 baja notablemente el índice de accidentes**. Puede tomarse como una anomalía pero teniendo en cuenta que fue año de lockdown es completamente esperable.

<p align="left">
<img src="Images\graph1.png" height=200>
</p>

Con respecto a las horas y días en que ocurren los siniestros, pude visualizar un dato muy importante: hay una gran **concentración de accidentes los días sábados y domingos por la madrugada**. Este dato me llevó a pensar en la movida nocturna famosa de Buenos Aires, y así es como comencé la recolección de otros dataset complementarios. 
Quise analizar los permisos de eventos masivos en la Ciudad pero el dataset encontrado era muy escaso (solo con registros del 2019). [anexo_I_eventos](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/anexo_I_eventos.ipynb)


**SINIESTROS Y LAS COMUNAS**

Sin olvidar el patrón encontrado en el punto anterior y queriendo investigar un poco más sobre la movida nocturna, analicé un segundo data set complementario que contiene registros de locales bailables de cada comuna de CABA. Para esto, extraje la información, realicé el ETL pertinente y comencé a cruzazr datos de lugares donde se concentran la mayor cantidad de siniestros los fines de semana con las comunas dónde hay más movimiento nocturno. Como era de esperar este analisis me brindó información nueva que me permitió obtener nuevas conclusiones.
Podemos decir que **la comuna 1 (barrioss: Constitución - Monserrat - Puerto Madero - Retiro - San Nicolás - San Telmo) es la comuna con más accidentes fatales y la comuna con más movida nocturna**. 

<p align="left">
<img src="Images\graph5.png" height=300>
</p>


En el siguiente link se encuentran los ETL realizados tanto al dataset de locales bailables como a un tercet dataset que utilicé para conocer más en profundidad los barrios y comunas de CABA: [anexo_II_comunas](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/anexo_II_comunas.ipynb)

Otros comportamientos encontrados: 
- Las comunas **1, 4 y 9 componen el top 3** de comunas con más accidentes. 
- El 71% de accidentes **ocurren en avenidas**.  


**SINIESTROS, VÍCTIMAS Y ACUSADOS**

Relacionando los accidentes viales con los implicados en los accidente (víctima y acusado) he podiro analizar métricas y comportamientos que sirven de input para la futura toma de decisiones. 
Pude observar que las víctimas son principalmente **peatones y conductores/acompañantes de motos de sexo masculino** y que la gran mayoría de acusados de los siniestros son **conductores de automóviles**
También pude observar que el rango de edad con más frecuencia entre las víctimas es de **20 a 40 años**, y que los accidentes más frecuentes se dan entre **moto y auto** y **peaton y colectivo**  

<p align="left">
<img src="Images\graph4.png" height=200>
</p>

## Diseño y creación del dashboard:  

Creé un dashboard interactivo en **PowerBi** mostrando todo el análisis realizado a través de gráficos pertinentes y coherentes para que sea sensilla la interpretación de los datos. Incluyte filtros permitiendo explorar detalladamente los datos con la selección de cada uno de ellos, incluye también tooltips para complementar la informacón y diversas pestañas que permiten navegar a través de estas tres secciones detalladas anteriormente.  


## Desarrollo de KPIs:  

Una de los desafíos planteados en el proyecto era la medición de 2 KPI planteados por la Ciudad de Buenos Aires, para poder medir de forma certera si los objetivos planteados fueron alcanzados. En este caso los dos KPI propuestos eran:
- Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior. 
- Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.

A estos dos KPIs le sumé uno planteado por mi que es necesario calcularlo para continuar con el análisis de los accidentes en horas de madrugada: 
- Reducir en un 10% la cantidad de accidentes mortales que se producen de madrugada en el último año, respecto al año anterior.
  
Podemos observar que el objetivo planteado en el KPI 2, en el año 2021, no se cumplió, a diferencia del objetivo en el KPI3 que si se cumplió ya que se logró disminuir en el 2021 más del 10% de los accidentes de madrugada     

<p align="left">
<img src="Images\kpis.png" height=250>
</p>



# <h3 align=left>**`CONCLUSIONES`**</h3>
- A través de este análisis exploratorio de los datos he podido observar como se comportan los registros de accidentes fatales en la Ciudad de Buenos Aires. 
- Puedo obtener como conclusión que los meses con más accidentes son los meses festivos, en dónde la población sale más de sus hogares y hay más actividades en la ciudad. Sin embargo las muertes por accidentes viales se registran a lo largo de todo el año, debiendo tomar medidas urgentes para bajar este índice. Observando también una baja en el número de accidentes fatales en el año 2020 disminuyó abruptamente debido al lockdown. 
- Observé a través del cruce de métricas que hay una gran concentración de accidentes fatales los fines de semana en la madrugada en comunas específicas, comunas que contienen mayor densidad de bares y locales bailables, por lo que se llama a una toma de medidas urgentes en cuanto a los controles de alcoholemia. 
- La mayor cantidad de accidentes se producen en avenidas de estas comunas y se observa que la mayoría de accidentes son provocados por autos. 
- En lo que respecta a las víctimas fatales, podemos observar que la mayoría son personas de sexo masculino, entre los 20 y 40 años. También pude observar un registro altísimo de peatones víctimas fatales de accidentes de tránsito por lo que se llama a tomar medidas en cuanto a la consientización del automovilista en el respeto del peatón.