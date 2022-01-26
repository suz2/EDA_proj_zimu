# Analysis between MTA Turnstile, weather condition and Covid New cases in Manhattan
Zimu Su

## Abstract

This project aims at exploring the trend of entries and exits number of MTA station in New York city as response to the local weather conditions and daily COVID new cases around year 2020 and 2021. The daily turnstile data collected at the MTA stations around times square are compared to temperature, precipitation measured at central park weather observation site and Covid new cases provided by New York Times. A consistent trend is discovered among the MTA riders, temperature, and COVID new cases, but reveals to be time dependent. The dependency might be caused by the number of available entries channels in the station in different periods.

## Design

MTA in New York faces shortage of workers during the COVID pandemic, while the MTA ridership number continues growing. It is necessary to optimize the staff resources based on the prediction of rider number under different daily situation, e.g., The project explores the potential relationship between daily entries/exits number at MTA station, local weather condition and growth of Covid cases in New York city.

## Data

*MTA Turnstile Data*
  * [Link: Turnstile](http://web.mta.info/developers/turnstile.html)
  * Apply selection of entries/exists value at four station 'TIMES SQ-42 ST', 'GRD CNTRL-42 ST', '42 ST-PORT AUTH' and '42 ST-BRYANT PK' at time "00:00:00" from date 01/01/20 to 12/31/21. The dateset has 84192 rows in total, containing the entries/exits data at each channel (scp) in the unit of the station.

*NOAA climate data*
  * [Link: Climate](https://www.ncdc.noaa.gov/cdo-web/)
  * The dataset contains daily maximum/minimum temperature, precipitation at central park observation site covered from 01/01/20 to 12/31/21。

*Covid statistics*
  * [Link: Covid statistics](https://github.com/nytimes/covid-19-data)
  * The dataset contains daily new cases, deaths in each county of United states.

## Algorithms

*Data Auditing*
* Entries/exits data is converted from odometer style to daily increment
* Find the time gap in which the data of station or subunit channel (scp) is lost
* Eliminate the reverse counted entries/exists value.
* Create datasets of daily enitries/exists, temperature, precipitation, Covid new cases.

*Analysis*
* Create plots describing the time trend of entries/exits number, temperature, covid new cases.
* Create plots displaying the relationship between entries/exits number and max/min temperature, precipitation, covid new cases.

## Tools

Pandas, SQLalchemy, SQLite, Matplotlib, Seaborn

## Communication

The project is under supervision of Julia Lintern and Tim Dooley. The presentation is made on 01/26/22.



