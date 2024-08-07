
# <h1 align=left> DATA ANALYTICS OPERATIONS </h1>
# <h3 align=left>**`Henry Bootcamp - Academic Experience`**</h3>
</b></b>  

<p align="center">
<img src="Images\portada.png" height=200>
</p>

# <h3 align=left>**`PROJECT DESCRIPTION`**</h3>

The `Mobility and Road Safety Observatory` (OMSV), a research center under the **Secretariat of Transport of the Government** of the Buenos Aires City, concerned about its very high traffic accident mortality rates, commissioned me to conduct a data analysis project on its traffic accident database for the period from 2016 to 2021. The goal was to decipher trends and patterns, understand vehicular behavior in the city, and make informed decisions.

[Mobility and Road Safety Observatory](https://buenosaires.gob.ar/movilidad/plan-de-seguridad-vial/observatorio-de-movilidad-y-seguridad-vial)

As the data analyst for the project, I carried out the following tasks:

- Data Cleaning and Preparation: I normalized and transformed the data to make it compatible and consistent. (DATA)
- Data Analysis: I applied statistical techniques and algorithms to explore and understand the data. (DATA)
- Identified patterns, trends, and relationships within the data. (INFORMATION)
- Data Visualization: I created a dashboard with graphs, tables, and other types of visualizations to represent the data in a comprehensible manner. (INFORMATION)
- Conclusions: I interpreted the results of the analysis and drew conclusions to help stakeholders make informed decisions. (KNOWLEDGE)

-----------------------------------------------------------------------------------------------------

# <h3 align=left>**`PROJECT STRUCTURE`**</h3>
- **Data:.csv** the repository contains the .csv files received (DB_seed), files with applied ETL (_ETL), and additional csv files used to deepen the EDA.
- **Notebooks:** the repository includes 4 Jupyter notebooks: one for ETL, one for EDA, and two supplementary notebooks that complement the EDA (ETL for additional databases).
- **Dashboard.pbix:** Power BI file with the interactive dashboard.
- **README.md:** Project description and guide.
 
-----------------------------------------------------------------------------------------------------

# <h3 align=left>**`TECH STACK`**</h3>
- Python: Main programming language.
- Pandas: Data manipulation and analysis.
- NumPy: Support for arrays and high-performance mathematical operations.
- Matplotlib and Seaborn: Graph creation.
- Power BI: Business intelligence tool for interactive data visualization and reporting.
- Jupyter Notebook: Interactive environment for writing and executing Python code, ideal for data analysis and visualization.


-----------------------------------------------------------------------------------------------------

# <h3 align=left>**`DATA SOURCES`**</h3>
**Main:**

- [Buenos Aires Data](https://docs.google.com/spreadsheets/d/1nq00jGIZHQ1RLSET43zKnUsMsoFb-pBg/edit#gid=1625530738)
- [Data dicionary](https://docs.google.com/spreadsheets/d/1Op98U-Hh2a3Q7uuznAzdl4Bf8r8qPr4m/edit#gid=1771770012)

**Complementary:**

- [Communes of Buenos Aires City](https://data.buenosaires.gob.ar/dataset/comunas)
- [Permits for massive events in the Buenos Aires City](https://data.buenosaires.gob.ar/dataset/permisos-eventos-masivos)
- [Dance venues in the Buenos Aires City](https://data.buenosaires.gob.ar/dataset/locales-bailables)


-----------------------------------------------------------------------------------------------------


# <h3 align=left>**`STEPS TAKEN`**</h3>
## Data Transformations:
I read the datasets in the correct format, as well as cleaned and preprocessed the data from the databases I later worked with.
I removed unnecessary columns, imputed null values, and analyzed outliers, among other procedures.
The transformations are documented in the notebook [ETL_PI2](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/ETL_PI2.ipynb)

## Exploratory Data Analysis:
I conducted an exploratory analysis of the data to better understand the relationships between variables, detect behavior and interesting patterns that could inform future decisions.
I created coherent graphs according to the type of variable, which provided valuable information to understand behaviors.
The entire process can be viewed in the following notebook: [EDA_PI2](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/EDA_PI2.ipynb)

It was essential to cross-reference the most important data we had (**number of victims: 715 in 6 years, only in CABA**) with various factors such as the passage of time, the neighborhoods of Buenos Aires, and data on victims and accused individuals. 


**ACCIDENTS AND THE TIME**

Through the analysis of the 6 years covered in the dataset, I observed both regular and atypical behaviors.
Among the regular behaviors, I found that the months with the highest number of fatal victims in Buenos Aires are the **last months of the year**. As for atypical behaviors, there is a noticeable decrease **in the accident rate in 2020**. This can be seen as an anomaly, but considering it was a lockdown year, it is entirely expected.

Regarding the times and days when accidents occur, I observed a very important data point: there is a **high concentration of accidents on Saturday and Sunday mornings**. This led me to consider Buenos Aires' famous nightlife, prompting me to collect additional complementary datasets.
Initially, I intended to analyze permits for mass events in the city, but the dataset I found was very limited (only records from 2019).
[Appendix_I_events](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/anexo_I_eventos.ipynb)

<p align="left">
<img src="Images\gif1.gif" height=300>
</p>


**ACCIDENTS AND THE NEIGHBORHOODS**

Without overlooking the pattern found in the previous section and wanting to investigate the nightlife further, I analyzed a second complementary dataset containing records of nightlife venues in each neighborhood of CABA. For this, I extracted the information, performed the necessary ETL, and began cross-referencing data from the locations with the highest concentration of accidents on weekends with the neighborhoods with the most nightlife activity. As expected, this analysis provided new insights that led to new conclusions.
We can say that **the Neighborhood 1 (areas: Constitución - Monserrat - Puerto Madero - Retiro - San Nicolás - San Telmo) is both the neighborhood with the most fatal accidents and the one with the most nightlife activity**.


<p align="left">
<img src="Images\graph5.png" height=300>
</p>

The following link contains the ETL processes performed on both the nightlife venues dataset and a third dataset I used to gain a deeper understanding of the neighborhoods and districts of CABA: [appendix_II_communes](https://github.com/PaulaDaher/Proyecto_DataAnalytics_CABA/blob/main/anexo_II_comunas.ipynb)

Other observed behaviors:
- Neighborhoods **1, 4, and 9 make up the top 3** neighborhoods with the most accidents.
- 71% of accidents **occur on avenues**.

<p align="left">
<img src="Images\gif2.gif" height=300>
</p>


**ACCIDENTS, VICTIMS, AND ACCUSED**

By relating traffic accidents to those involved (victims and accused), I was able to analyze metrics and behaviors that provide input for future decision-making:
- I observed that the victims are primarily **pedestrians and male motorcycle riders/ passengers**, and that the majority of those accused in the accidents are **car drivers**.
- I also found that the most common age range among the victims is **20 to 40 years**, and that the most frequent types of accidents occur between **motorcycles and cars and pedestrians and buses**.


<p align="left">
<img src="Images\graph4.png" height=200>
</p>


## Dashboard Design and Creation:  

I created an interactive dashboard in **PowerBi** showing all the analysis conducted through relevant and coherent graphs to facilitate data interpretation. It includes:
- Filters allowing detailed exploration of the data by selecting each one
- Tooltips to complement the information
- KPI analysis
- Various tabs enabling navigation through the three sections detailed above. 

<p align="left">
<img src="Images\gif3.gif" height=300>
</p>

</b>

## KPI Development:  

One of the challenges posed in the project was measuring two KPIs established by the City of Buenos Aires to accurately assess whether the objectives were achieved. The two proposed KPIs were:

- Reduce the traffic accident homicide rate by 10% in the last six months in CABA compared to the homicide rate in the previous semester.
- Reduce the number of fatal motorcycle accidents by 7% in the last year in CABA compared to the previous year.

I also added a KPI that I proposed, which is necessary to calculate in order to continue analyzing accidents during early morning hours:
- Reduce the number of fatal accidents occurring during early morning hours by 10% in the last year compared to the previous year.
We can observe that the objective set for KPI 2 was not met in 2021, unlike KPI 3, which was achieved as the number of early morning accidents was reduced by more than 10% in 2021.

</b></b>

<p align="left">
<img src="Images\kpis.png" height=250>
</p>


# <h3 align=left>**`CONCLUSIONS`**</h3>  

- Through this exploratory data analysis, I have observed how fatal accident records behave in the City of Buenos Aires.
- I can conclude that the months with the highest number of accidents are the festive months when the population is more active and there are more activities in the city. However, traffic accident fatalities occur throughout the year, indicating a need for urgent measures to reduce this rate. It is also noted that the number of fatal accidents in 2020 dropped sharply due to the lockdown.
- By cross-referencing metrics, I observed a significant concentration of fatal accidents on weekends during early morning hours in specific neighborhoods, which have a higher density of bars and nightlife venues. This calls for urgent measures regarding alcohol testing.
- Most accidents occur on avenues in these neighborhoods, and it is observed that the majority of accidents are caused by cars.
- Regarding fatal victims, it is observed that most are male, aged between 20 and 40 years. There is also a very high record of pedestrian fatalities, which calls for measures to increase driver awareness and respect for pedestrians.