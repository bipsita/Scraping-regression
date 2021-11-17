# Does weather affect transit ridership? A study of the MTA bus and subway system

## Abstract
On days of extreme weather, transit riders likely shift to door-to-door modes such as private cars, Uber, & Lyft. It might be worthwhile for transit authorities to invest in infrastructure such as weather-controlled transit stops and shelters, and possibly a motorized mode that protects against the elements, to provide the last mile service. This study applies a linear regression model to investigate the effect of weather on transit ridership of the MTA system. Weather was found to affect holiday riders more than daily commuters, and decreases in temperatures seemed to affect MTA ridership more adversely than increases.

## Design
The literature on transit ridership mostly finds service attributes such as frequency and number of routes to have a strong influence on ridership. At an aggregate level, population and employment are the main features. We aim to study the effect of extreme weather on transit ridership by using data obtained for the duration March 2020 to September 2021 through web-scraping, and that downloaded from the MTA website.

## Data
The weather data provided 16 features of which maximum, minimum, and average temperature, precipitation, and wind speed was selected. The MTA data consisted of the number of bus and subway riders on the various dates. 

## Algorithms
**Feature Engineering**
1. Days of the week, seasons, and federal holidays were obtained from the dates studied.
2. Categorical variables such as seasons, weekdays, and weekends were converted to binary dummy variables. 
3. Polynomial variables were obtained by interacting different related variables.

**Models**

A linear regression model was estimated over the initial dataset of 16 features and 1174 rows of data. The dataset was split into a 33/66 train/test set. K-fold validation was conducted on the training data set holding out the test for the final score. 

**Scores**
- Score on training set: 0.37
- Mean score on validation set: 0.32
- Score on test set: 0.33
- MAE: 330691 (mean ridership 1228343)

Lower test and validation scores indicates presence of outliers. Overall low score indicates that there were other significant variables that have not been captured. Dates of PAUSE orders due to Covid and dates since vaccines became available is one such major data source. Additionally, this is time-series count data with a large number of zeros.   

## Tools
- Selenium and BeautifulSoup for web-scraping
- Numpy and Pandas for data manipulation
- Scikit-Learn and Statsmodel for modeling
- Matplotlib and Seaborn for plotting
