# Exploratory Data Analysis

All the python notebooks are already executed and the inputs used for the data visualization are present in the resources folder. Jupyter Notebook is needed to view the ipython files. Just download the ipython notebooks and view the data visualization by launching the jupyter notebook.

### Sample.ipynb

Contains sample code for getting started with R programming language, using their dataset, importing files, demonstrating ggplot, maptools etc

### Flu EDA.ipynb

Seasonal Flu data of 2017-2018 was collected from Centers for Disease Control and Prevention (https://gis.cdc.gov/GRASP/Fluview/PedFluDeath.html) and based on the data following data visualizations were made using Plotly.

1. Influenza Positive Tests for type A and type B Flu (per week) along with the positive percentage. (Based on U.S. Clinical Laboratories data)
2. Influenza Positive Tests for various types of flu per week. (Data based on Public Health Laboratories, National Summary,2017-18 Season)
3. Flu heat map of USA (Data based on U.S. Outpatient Influenza-like Illness Surveillance Network)
4. Pneumonia and Influenza (P&I) Mortality Surveillance with the percentage of death, baseline and threshold. (National Center for Health Statistics) 
5. Percentage of Visits for Influenza-like Illness (ILI) along with the national baseline of 2.2 (Data based on U.S. Outpatient Influenza-like Illness Surveillance Network)
6. Influenza sub-type pie-charts

### Twitter.ipynb

The heat map generated from the CDS data reported by Data based on U.S. Outpatient Influenza-like Illness Surveillance Network was compared with the real time twitter data. Tweets based on tags were collected along with their location data using the rtweet package and same heat map was generated and compared. The tags used for retrieving the tweets are flu, flu no work, flu down ,flu vomiting ,flu coughing ,flu with sick ,flu Fatigue ,flu Headache ,flu diarrhea ,flu fever ,flu season.

#### Used rtweet and twitter API keys to fetch data from twitter:
1. Load the OAuth details
2. Load the word to be searched
3. Fetched the twitters and saved them as csv
4. The twitter data contains two files, one the tweets and other the user information
5. Since the location from tweets is mostly NA, use location from user information to get the latitude and longitude of the user
6. Even in the location information of the user, if there user had entered an non standard address google geocode api might give n/a for few locations
7. After filtering all the unwanted data use the rev geocode to get the address which contains the state information
8. Parse the address and get the State Information
9. Filter the state information which belong to non USA state values
10. Using the value plotted the USA Heat Map

#### Conclusion
Analysising the data collected from Twitter we could see that California, Texas, Kansas, Illinois, Florida were indeed matching with data analysised from CDS. However, the same cannot be said for other states. Personally, I believe this variation is because people the above mentioned states had twitted while others were trying to recover from the flu.
