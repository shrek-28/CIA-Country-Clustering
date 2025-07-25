# Country Clustering using KMeans Clustering 

## Introduction 
The CIA World Factbook Country Clustering dataset provides a rich collection of socioeconomic, geographic, and demographic indicators compiled by the CIA for countries across the globe. This data is ideal for unsupervised learning tasks, especially clustering, to group countries based on shared characteristics like economy, population, geography, and military. It can help uncover regional patterns, development tiers, or geopolitical groupings.

Clustering can reveal which countries are similar in terms of development, resources, or strategic metrics, without any prior labels.

### Feature Descriptors 
| Column                                 | Description                                                                                                                           |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Country**                            | Name of the country (string).                                                                                                         |
| **Region**                             | Geopolitical or continental region (e.g., Asia, Europe). Used for grouping or color coding in visualizations.                         |
| **Population**                         | Total population of the country (integer).                                                                                            |
| **Area (sq. mi.)**                     | Land area of the country in square miles (integer).                                                                                   |
| **Pop. Density (per sq. mi.)**         | Population per unit area – a measure of how crowded a country is.                                                                     |
| **Coastline (coast/area ratio)**       | Ratio of coastline length to land area – higher values indicate more coastal access relative to land size.                            |
| **Net migration**                      | Number of people entering minus those leaving the country per 1,000 population – a positive number means more people are immigrating. |
| **Infant mortality (per 1000 births)** | Number of infants dying before age 1 per 1,000 live births – an indicator of healthcare quality.                                      |
| **GDP (\$ per capita)**                | Gross Domestic Product per person – a basic measure of national economic wealth.                                                      |
| **Literacy (%)**                       | Percentage of the adult population that can read and write – a core education indicator.                                              |
| **Phones (per 1000)**                  | Number of landline/cell phones per 1,000 people – a proxy for infrastructure and connectivity.                                        |
| **Arable (%)**                         | Percentage of land suitable for farming – an agricultural resource indicator.                                                         |
| **Crops (%)**                          | Percentage of land used for permanent crops.                                                                                          |
| **Other (%)**                          | Percentage of land not used for crops or arable farming – includes forests, deserts, cities, etc.                                     |
| **Climate**                            | Numerical representation of average climate type (e.g., tropical, temperate). May need mapping to descriptions.                       |
| **Birthrate**                          | Number of births per 1,000 population – higher rates are often associated with developing nations.                                    |
| **Deathrate**                          | Number of deaths per 1,000 population – may correlate with age distribution and healthcare.                                           |
| **Agriculture**                        | Proportion of GDP contributed by the agriculture sector – indicates economic dependence on farming.                                   |
| **Industry**                           | Proportion of GDP from industrial sectors (manufacturing, mining, etc.).                                                              |
| **Service**                            | Proportion of GDP from service sectors (education, finance, healthcare, etc.).                                                        |

## Methodology 
1. The initial data analysis was conducted using ```df.info```, ```df.head()``` and ```df.describe``` to verify data types, understand features, and obtain initial statistical feature-wise analysis of the data.
2. Univariate analysis of population was conducted, using histograms.
3. Bivariate analysis was conducted between different variables, using scatterplots and bar charts.
4. A correlation heatmap was used to visualize all bivariate relationships in one single plot.
5. Data was cleaned through filling up null values, dropping columns and imputation. The final cleaned dataframe was exported as a .csv file.
6. The data was scaled using ```StandardScaler()```.
7. The KMeans Model was trained for different K values, and an elbow plot was used to determine the ideal number of clusters.
8. The data was finally fitted into a 100 clusters. 
