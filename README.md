# US-Air-Quality-Trend

## Part 1: Introduction 

### 1.1. Problem Statement

Our goal is to illustrate trends in air quality in the United States, identifying which pollutants have contributed most to air quality changes over the years. Our analysis will include how weather, natural disasters, and select world events affect air quality as measured by the U.S. Environmental Protection Agency (EPA). We will use Google Cloud Platform's (GCP) Dataproc service to distribute and interact with daily air quality information from the EPA's Historical Air Quality data set (hosted on BigQuery) which includes data from collection points across the U.S. dating back to 1990.

### 1.2. Motivation

Air pollution is a significant problem with adverse health outcomes, so understanding air quality trends is crucial for effective management strategies. In this study, we explore six pollutants that were key drivers of the 1990 Clean Air Act whose standards brought about the generation of our data set. We chose this problem based on our knowledge that historical air quality data can identify sources of pollution, inform targeted interventions, and aid in the development of evidence-based approaches that promote environmental sustainability and protect public health.

### 1.3. Data Source

The EPA Historical Air Quality data set is hosted here on __[Google Cloud Platform](https://console.cloud.google.com/marketplace/product/epa/historical-air-quality)__.

## Part 2: Challenges

### 2.1. Computing

The first challenge we encountered was related to computing. Given that we needed to deal with six tables, it became necessary for our cluster to scale up in order to run multiple notebooks which can be computationally expensive. To address this challenge, we decided to append the six tables together. This approach simplified the data processing pipeline and reduced the computational load, thereby enabling more efficient analysis.

### 2.2. Data Wrangling

The second challenge was related to data wrangling. We first chose six pollutants based on the information provided by [AirNow](https://www.airnow.gov/aqi/aqi-basics/). They are Ground-level Ozone, Particle Pollution (including PM2.5 and PM10), Carbon Monoxide, Sulfur Dioxide, and Nitrogen Dioxide. Each pollutant has distinct measurements that need to be analyzed separately, which made data wrangling a complex task. Our approach was to develop a standardized data cleaning and preprocessing pipeline that could be applied uniformly across all pollutants. In this way, we can ensure that our analysis is accurate and reliable.

## Part 5: Conclusions and Future Scope

From the first phase of our study on the EPA Historical Air Quality data set, we learned that the EPA monitors air quality across the United States with 3,327 distinct measurement sites.  Our data set includes measurement from 1990 to 2022.

Since the inception of the Clean Air Act of 1990, air quality has drastically improved in aggregate across the United States. This is indicated by steep declines in daily measurements of Carbon Monoxide (CO), Sulfur Dioxide (SO2), Nitrogen Dioxide (NO2), and Particulate Matter 2.5 (PM2.5) and 10 (PM10), although Atmospheric Ozone (O3) has remained fairly constant in recent history. It is worth noting that the standard deviation for NO2, SO2, and PM2.5 and PM10 were much higher in comparision with CO and O3. 

We know, however that the Clean Air Act of 1990 is not the only legislation enacted in the U.S. to restrict pollutants, so in the next version of this notebook we will look more closely at California whose legislature passed additional Ambient Air Quality Standards in 2002, 2006, and 2008 (California Air Resources Board). Our early exploratory data analysis revealed that California leads all other U.S. States in climate events that may impact air quality. These events include things like wildfires, earthquakes, and volcanic activity. In an effort to better understand the interaction of air quality and events, we will conduct future analyses into the immediate aftermath of events that caused an observable spike in AQI. 

Finally, we demonstrated the seasonality of most pollutants, which may be an indicator that temperature and wind also influence airborne concentrations of pollution with changing seasons.  This will also be focal point of our future work.
