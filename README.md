
# <h1 align=left> DATA ANALYTICS OPERATIONS </h1>
# <h3 align=left>**`PAULA DAHER`**</h3>

<p align="center">
<img src="image.png" height=300>
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


### El proyecto lo dividí en dos partes:

**Parte I:** ETL / EDA
Se empieza desde cero, haciendo un trabajo rápido de Data Engineer con la recolección y extracción de datos de archivos, así como sus tratamiento, transformación y modelado. 
En esta línea, hay varios aspectos indispensables que **deben** ser abordados en cualquier Análisis Exploratorio de Datos y tomaremos como punto de partida para evaluar tu performance en este apartado. Entre estos aspectos destacados se encuentran: *búsqueda de valores faltantes, valores atípicos/extremos u outliers y registros duplicados*. Asimismo, la utilización de gráficos coherentes según la tipología de variable que corresponda resulta esencial.

**Parte II:** Creación de dashboard en PowerBi / análisis de KPIs
Se crea el modelo, se consumen los datos ya limpios, y se entrenar bajo ciertas condiciones. Como resultado se crea un sistema de recomendación de videojuegos para usuarios de Steam, utilizando técnicas de MLOps para asegurar que el modelo y la API sean escalables, reproducibles y mantenibles.
Debe ser funcional y coherente con el storytelling. El dasbhoard tiene que incluir **filtros**, permitiendo explorar detalladamente los datos con la selección de cada uno de ellos. Es decir, es indispensable que sea **interactivo**. También, se espera que el diseño que implementen facilite la interpretación de la información y su análisis, siendo importante, para ello, la claridad en la presentación de los datos, aspectos inherentes a la esteticidad, elección coherente de los gráficos según las variables a visualizar, entre otros ítems. 
Debes graficar y medir los 2 KPIs propuestos a continuación, representándolos adecuadamente en el dashboard. A su vez, tambíen tienes que proponer, medir y graficar un tercer KPI que consideres relevante para la temática. 


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
1. Transformaciones de Datos:  
Se realizó la lectura de los dataset en el formato correcto, se realiza la limpieza y preprocesamiento de los datos de las bases sobre las cuales se trabajó. 
Se eliminaron columnas innecesarias, se imputaron valores nulos y datos anidados entre otras cosas.   
Las transformaciones se encuentran asentadas en el notebook [ETL_PI2](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/ETL_PI2.ipynb)

2. Análisis Exploratorio de Datos (EDA):  
Se realizó un análisis exploratorio de los datos para entender mejor las relaciones entre las variables, detectar outliers y patrones interesantes.


- Cruce de datos con datasets complementarios, ya sea para obtener información nueva o poder comparar la información disponible para todas las plataformas. 


3. Desarrollo y diseño de dashboard:  
Se desarrolló un sistema de recomendación basado en la similitud del coseno:
 - Input: ID de un producto.
 - Output: Lista de 5 juegos recomendados similares al ingresado.




4. Desarrollo de KPIs:  
Se implementaron los siguientes endpoints en la API utilizando FastAPI:
 - **developer(desarrollador: str):** Cantidad de items y porcentaje de contenido Free por año según empresa desarrolladora.
 - **userdata(User_id: str):** Cantidad de dinero gastado por el usuario, porcentaje de recomendación y cantidad de items.
 - **UserForGenre(genero: str):** Usuario con más horas jugadas para el género dado y acumulación de horas jugadas por año de lanzamiento.
 - **best_developer_year(año: int):** Top 3 de desarrolladores con juegos más recomendados por usuarios para el año dado.
 - **developer_reviews_analysis(desarrolladora: str):** Análisis de reseñas de usuarios categorizados con análisis de sentimiento (positivo o negativo).
 - **recomendacion_juego(id de producto: str):** Lista de 5 juegos recomendados similares al ingresado.


# <h3 align=left>**`CONCLUSIONES`**</h3>

- A través de este análisis exploratorio de los datos he podido observar como se comportan los registros de accidentes fatales en la Ciudad de Buenos Aires. 
- Puedo obtener como conclusión que los meses con más accidentes son los meses festivos, en dónde la población sale más de sus hogares y hay más actividades en la ciudad. Sin embargo las muertes por accidentes viales se registran a lo largo de todo el año, debiendo tomar medidas urgentes para bajar este índice. Observando también una baja en el número de accidentes fatales en el año 2020 disminuyó abruptamente debido al lockdown. 
- Observé a través del cruce de métricas que hay una gran concentración de accidentes fatales los fines de semana en la madrugada en comunas específicas, comunas que contienen mayor densidad de bares y locales bailables, por lo que se llama a una toma de medidas urgentes en cuanto a los controles de alcoholemia. 
- La mayor cantidad de accidentes se producen en avenidas de estas comunas y se observa que la mayoría de accidentes son provocados por autos. 
- En lo que respecta a las víctimas fatales, podemos observar que la mayoría son personas de sexo masculino, entre los 20 y 40 años. También pude observar un registro altísimo de peatones víctimas fatales de accidentes de tránsito por lo que se llama a tomar medidas en cuanto a la consientización del automovilista en el respeto del peatón.