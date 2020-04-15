# Data Preparation and Visualization

## Data Preparation
For the data preparation part, our team mainly collect and construct two datasets. 

The first dataset contains daily COVID-19 cases, including confirmed, death and recovery, at state level for U.S.

The second dataset contains information of US states regarding education, medical resource, public transportation, social distancing, aging and population density.
### COVID-19 dataset
Our team has built a pipeline to get and clean the latest data at state level from [CSSE daily report](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports).

Here is an overview of our COVID-19 cases dataset:


### US state information dataset
First, we have collected information from various sources and aggregate those information at a state level to generate this dataset.

Then our team identified each time spot for the change of social distancing status in a state and split the whole time period based on these time spots. In this way, we can better see the impact of social distancing status on the spread of COVID-19 virus.

Here is an overview of our US state information dataset:

## Data Visualization
Here is the codes for the visualizations we made using Python.