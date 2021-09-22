# Regression Project Proposal

## Question/Need
Broad question: what are the various factors that influence transit ridership? Within that, we have narrowed down on: what is the effect of weather and of service changes on transit ridership? With weather becoming more extreme, the answer to this question will help transit authorities decide what extent of shelter transit stops and stations should have, and also how patrons could be connected to those. For the service changes question, transit authorities may consider whether it may be wise to spend more to expedite repair or have a larger backup crew to encourage ridership.

## Data Description
Depending on ease of scraping, there is one of two alternative datasets that I will use:
### 1. MTA turnstile users:
* Number of users (target)
from http://web.mta.info/developers/turnstile.html for one month, August -September 2021; 
* Service change information from mymtaalerts.com/ma;
* weather information from https://www.wunderground.com/history/monthly/KLGA/date/2021-9.

I will combine the data at from different turnstiles to obtain the individual sample/unit of analysis as the ridership every four hours in the entire system (target). I will work with maximum, minimum, and average temperature, precipitation, day of the week, time of the day, and total number of each of the following in the system:
stop closures, line closures, elevators out of service, vehicles out of service.
### 2. AC Transit bus users:
* Number of users (target) from data that I have collected earlier from AC Transit for July 2020. 
* Service change information from https://www.actransit.org/service-notices?page=0
* weather information from https://www.wunderground.com/history/monthly/us/ca/oakland/KOAK

I will combine the data from the different bus stops to obtain the individual sample/unit of analysis as the four hourly ridership in each major city and surroundings (target) Berkeley, Oakland, San Francisco, and one city South of Oakland (Fremont). The features are the same as for alternative 1. 

## Tools
I plan to use BeautifulSoup, Selenium, or Scrapy as needed. I would like to use advanced visualization or production tools if there is time.

## MVP Goal
My MVP goal for this project is to have a basic regression model with the target and some features. 






