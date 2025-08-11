# Infectious-Disease-Outbreak-and-weather-Patterns
  An epidemiological record focused on disease outbreaks, specifically Acute Diarrhoeal Disease, in India.

It includes the following columns:
SI No.: A unique identifier for each entry (e.g., 0).
Week of Outbreak: The week of the recorded outbreak (e.g., 1st week).
State: The state where the outbreak occurred (e.g., Meghalaya).
District: The specific district within the state (e.g., East Jaintia Hills).
Disease: The disease type (e.g., Acute Diarrhoeal Disease).
Cases: The number of reported cases (e.g., 160).
Deaths: The number of deaths (e.g., 0).
Day: The day of the outbreak (e.g., 2).
Month: The month of the outbreak (e.g., 1 for January).
Year: The year of the outbreak (e.g., 2022).
Latitude: The geographical latitude (e.g., 25.25).
Longitude: The geographical longitude (e.g., 92.48).
Precipitation: The amount of precipitation (e.g., 0.02).
Temp: The temperature (e.g., 29.53).

1. EDA & Dashboard using Excel
	
        •	Data Cleaning:
             Assigned SI No. to all rows
		           Handle missing values under 
                    5 null district and replaced it with state names
                    6431 deaths with zero 
             Formated data types correctly (dates, numbers, text)
                    Range: The range of cases (e.g., HIGH).
                    YES/NO: Indicates presence or absence of a specific condition (e.g., NO).

	       •	EDA Tasks:
		           Used pivot tables and charts to summarize data
		           Calculated key statistics 
                    mean, median, mode for cases
                    count for different diseases
                    min, max for temperature (Min-Max of Temperature: The temperature range (e.g., 47% or possibly 4-7°C, depending on formatting).

	        •	Dashboard Creation:
	            Key metrics (KPIs)
		                 Bar, line, pie, boxplots,pie, bubble charts
		                 Filters (using slicers) to visualize cases in different regions and death rates.




3. EDA & Visualization using Python

This repository contains a Jupyter Notebook (Infectious Disease Outbreak and weather Patterns.ipynb) that analyzes a dataset on
 infectious disease outbreaks in India from 2009 to 2022, integrated with weather patterns (precipitation and temperature). 
The analysis explores epidemiological trends, geographical hotspots, temporal patterns, and potential correlations between 
outbreaks and environmental factors. The notebook includes data loading, cleaning, feature engineering, statistical summaries, 
and visualizations.
The dataset focuses on diseases like Acute Diarrhoeal Disease, Malaria, Dengue, Chikungunya, Cholera, 
and Acute Encephalitis Syndrome, with ~8,985 outbreak records totaling ~842,087 cases and 291 deaths.

         •        Libraries:
                    pandas
                    numpy
                    matplotlib
                    seaborn (inferred from visualization code like sns.boxplot)

          •      Installed dependencies:
                    textpip install pandas numpy matplotlib seaborn

          •      Prepare the Dataset:
                    Placed Infectious Disease Outbreak and Weather Patterns.csv in the notebook's working directory or update the file path in the code cell:
                    textdf = pd.read_csv(r"path/to/Infectious Disease Outbreak and Weather Patterns.csv")

          •      Performed data description (head, info, describe).
                    Handled missing values and feature engineering.
                      5 null district and replaced it with state names
                      6431 deaths with zero 
                    Computed summaries (e.g., average cases by disease).
                      Range: The range of cases (e.g., HIGH).
                      YES/NO: Indicates presence or absence of a specific condition (e.g., NO).        
                      Adds 'Range' based on case thresholds.
                      Normalizes temperature to 'min-max of temp'.
                      Groups data for averages (e.g., cases by disease).

          •      Visualizations:
                     Generates visualizations using plots such as Bar, line, pie, bubble, area, boxplots charts
                     Boxplot: Temperature Distribution by Disease (e.g., variations across diseases like Malaria vs. Dengue).
                     (Inferred from code patterns): Correlation heatmaps, bar plots for disease frequency, line plots for cases over time, scatter plots for geospatial analysis (lat/long vs. cases), boxplots for precipitation by disease.
 
          •      Analysis:
                     Correlations: Weak links between cases and weather (e.g., preci ~ -0.018, temp ~ +0.001).
                     Trends: Declining outbreaks post-2016; seasonal spikes post-monsoon.
                     Hotspots: Maharashtra (1,195 outbreaks), Karnataka (1,097).



3. Power BI Project (with EDA, Data Modeling, DAX)


         • Data Import & Cleaning:
              Imported Final.csv using Power Query and removed duplicates with "Remove Duplicates".
              Handled nulls (e.g., "Deaths") by replacing with 0 using "Fill" in Power Query.

         • EDA in Power BI:
              Explored trends with bar charts (cases by year), line graphs (weekly cases), and tables (state-wise summary).
              Added filters and slicers for interactivity (e.g., year, state_ut).

         • Data Modeling:
               Created relationships between tables (if multiple) using "Manage Relationships".
               Applied a star schema with "state_ut" as a dimension table and outbreak data as a fact table.
               Set "SI No." as the primary key and linked it to foreign keys where applicable.

         • Dashboard Creation:
               Designed an interactive layout with slicers, KPIs (Total Cases, Average Temp), and visuals (map, bar, line charts).
               Ensured readability with clear titles, legends, and relevant filters.
