# Portfolio1_Python_MarketStudy

Here I show my data analysis skills in python with a case study on chicken export. 
The project was coded in Jupyter Lab and the notebooks are the files [Nb1_Data_Preparation.ipynb](https://github.com/VivienPichon/Portfolio1_Python_MarketStudy/blob/main/Nb1_Data_Preparation.ipynb) and [Nb2_Analysis_PCA_clustering.ipynb](https://github.com/VivienPichon/Portfolio1_Python_MarketStudy/blob/main/Nb2_Analysis_PCA_clustering.ipynb). 
The main steps and results were presented during a defense in which I used [the following slides](https://github.com/VivienPichon/Portfolio1_Python_MarketStudy/blob/main/Presentation_Slides_MarketStudy.pdf).

## Roleplay context

In this exercise, I am working for a French chicken producer. The company has been selling chicken on the national market and wants to start exporting, they ask me to find the best countries to start exporting their products.

I am specifically asked to make this analysis with a PCA on at least 12 variables, followed by a clustering.

## Main tasks
### Notebook 1

- Find the data with at least 8 indicators and indexes relevant to the chicken market of many countries,
- Clean and prepare the data, fill the NAs and have a minimum of 100 countries to work with,
- Calculate at least 3 new variables,

### Notebook 2

- Compute the PCA after choosing the number of components,
- Select a clustering algorithm, with parameters based on their relevant metrics,
- Visualize the clustered PCA results,
- Conclude on the best countries to start exporting to.

## Data Sources

Here is a list of the indicators and indexes I used and their sources. For each of these markers, I used the data of the year 2021 because it was the last year which was not affected by the major geopolitical and logistical disruptors that are the war in Ukraine and the Huthis attacks on ships in the Red Sea. The indexes which could not be found for the year 2021 were replaced with values for the closest earlier available values.

[**The World Bank**](https://data.worldbank.org/Tean)
- GDP in dollars
- Index of ease of business (2019)
- Logistics performance index (2018)
- Political stability index
- Population per country
- Consumer price index

[**Food and Agriculture Organization**](https://www.fao.org/faostat/en/#data)
- Chicken consumption per country
- Chicken import quantity
- Chicken import value

[**Transparency International**](https://www.transparency.org/en/)
- Corruption Perception Index

[**United States Department of Agriculture**](https://www.usda.gov/about-usda/reports-and-data/data/usda-open-data-catalog)
- Share of customer expenditure spent on food (marker dropped in the analysis because too many countries were missing)
