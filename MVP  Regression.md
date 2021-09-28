# MVP: Analysis of variation of MTA subway & bus use with change in weather 
We are studying daily usage of the MTA subway and bus system by users between March 1st 2020 to September 23, 2021, and downloaded the data from https://new.mta.info/coronavirus/ridership.
The daily weather data was downloaded from https://www.wunderground.com/history/monthly/us/ny/new-york-city/KLGA. Since our objective is to model the influence of weather on transit ridership, we chose MTA over the AC Transit summer data, as New York over 1.5 years would record greater temperature changes than a Bay Area summer. We did not scrape the service change data as it involved text analysis, and also the weather monthly table included complex formatting that used up the time allotted for scraping. 

Our model includes the following:

Target: Daily ridership of the entire MTA subway & bus system

Features: 
- Temperature of the day (maximum, average, minimum), 
- Average wind speed,
- Precipitation, 
- Subway/bus dummy

While the scraped table included maximum, minimum, and average information for humidity, pressure, and dew point, we hypothesize that those will have very little effect on MTA and bus ridership. 

The pairplot and heat map obtained are shown below:github.com/bipsita/Scraping-regression/blob/main/heatmap.png
github.com/bipsita/Scraping-regression/blob/main/pairplot.png
Each show very little influence of the different weather variables on the target which may be expected for everyday commute trips. I will next use a dummy for weekend and holiday trips, and interact it with the bad weather days (precipitation, low average temperature), to study the effect. I will also include long weekends and holidays. 

Next steps following feature engineering (stretch goals):
- include lagged ridership as a feature to account for the time-series effect
- Model the data using Facebook Prophet
- Include Covid information such as status of the governor's PAUSE order, vaccines becoming available etc. 
