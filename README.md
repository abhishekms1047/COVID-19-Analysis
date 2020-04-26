# COVID-19 Analysis
## Analysis Overview
This project is to conduct analysis on COVID19-related data to extract factors that may have influence on the spread of COVID-19 virus.

Our team has first built an automated pipeline to aggregate and clean the latest COVID-19 data at state level.
Then we have aggregated other data, such as medical resources index, social distancing index, etc, into our dataset for futher analysis.

After preparing the data, we conducted some basic visualizations on the data and have found that social distancing may have a huge impact on spread of COVID-19 by comparing the virus trends of California and New York.

To further verify our findings from a more comprehensive perspective, we bulit linear regression model to quantitatively measure these factors' impact on infection and death rates.

In the end, we reach the conclusion that gathering ban, education level, aging level in one area may have great impact on the spread of COVID-19 virus and made corresponding recommendations based on the results.

## Data Preparation
Our team has obtained most of the data from public sources and conduct some further processing and cleanning so that they would be proper for our analysis and modeling.

### Data Source
The raw data we collected for analysis are gathered from the following sources:

* COVID-19 data: Built a pipeline to get and clean the latest data at state level from [CSSE daily report](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports).

* Medical resource data: 1) Download state-level medicare disparity from [Data.Medicare-link2](https://data.cms.gov/mapping-medicare-disparities) and surgical quality from [Data.Medicare-link1](https://data.medicare.gov/Hospital-Compare/Ambulatory-Surgical-Center-Quality-Measures-State/axe7-s95e/data).  2) Extract country-level health index data from [WHO](https://www.who.int/data/gho) through its API.3)Mannually scrap other information from [GHDx](http://ghdx.healthdata.org/record/ihme-data/gbd-2016-healthcare-access-and-quality-index-1990-2016)

* Aging data: Mannually scrap data from [census.gov](https://data.census.gov/cedsci/profile?q=California&g=0400000US06&tid=ACSDP1Y2018.DP05)

* Popularity density data: Mannually scrap information from [wikipedia](https://simple.wikipedia.org/wiki/List_of_U.S._states_by_population_density)

* Basic geographic data: Mannually scrap information from [wikipedia](https://en.wikipedia.org/wiki/List_of_U.S._states_and_territories_by_area)

* Airpots index data: Mannually scrap data from [globalair](https://www.globalair.com/airport/state.aspx)

* Education index data: Mannually scrap information from [USA.com](http://www.usa.com/rank/us--average-education-index--state-rank.htm)
* Social distancing index: Get data file from [KhakiEconomics](https://github.com/khakieconomics/covid_data)
### Final dataset description
Our team has generated two final datasets.

The first one contains all the information, such as medical resource, education, etc, information for states in US.

The second one contains the latest COVID19 data,including confirmed, death, recovered cases, for each state in US.

## Data Visualizations
### COVID-19 Overview in US
![COVID-19 situations in US](https://github.com/Mandy-Gu/COVID-19-Analysis/blob/master/US_case_visualization.png?raw=true)

From the above graphs, we can see that the COVID-19 situations is most serious in California in west coase and in New York in east coast. So we have picked these two states for deeper visualizations and analysis.
### COVID-19 trends in California and New York
![COVID-19 trends in CA and NY](https://github.com/Mandy-Gu/COVID-19-Analysis/blob/master/COVID-19-trends-for-NY-and-CA.png?raw=true)

As we can see from the above graph, CA starts social distancing before things get worse and the new confirmed cases stay at a stable level while NY didn't start social distancing until there are quite a lot confirmed cases, which results in a different situations compared to CA.

## Modeling
After gaining some insights from our visualizations and analysis, we applied machine learning techniques to further quantitatively analyze the impact of those factors, such as social distancing, medical resource, etc.

### Modeling process
Our team has built a linear regression model to try to explain what factors can lead to infection rate.

The independent variables for both models are standarized index about education, medical resource, public transportation, social distancing, aging and population density.

### Modeling results
Population aging and surprisingly education index are the most influential factors in the COVID-19 spread in the U.S. Both these variables have statistically significant p-values and big coefficients.
