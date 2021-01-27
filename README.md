## CMPE255-Statistics of Airplane Crash Data

## Team Members
1. Sowmya Jupally 
2. Laxmi Prasanna Palle
3. Sandeep Reddy Bhimireddy
4. Sai Krishna Nandikonda
 
### 1) Project title
 Statistics of airplane crash data 
 
### 2) What data you’ll use and where you’ll get it?
 https://data.world/data-society/airplane-crashes

 This dataset contains a full history of airplane crashes from 1908 to present which resulted in deaths throughout the world from civil, military, aviation, etc. 
 
 
### 3)Description of the problem you’ll solve or the question you’ll investigate. 
1) Yearly how many planes crashed? How many people were on board? How many survived? How many died?
2) Highest number of crashes by operator and Type of aircrafts.
3) ‘Summary’ field has the details about the crashes. Find the reasons of the crash and categorize them in different clusters i.e Fire, shot down, weather (for the ‘Blanks’  in the data category can be UNKNOWN) you are open to make clusters of your choice but they should not exceed 7. 
4) Find the number of crashed aircrafts and number of deaths against each category from the above step. 
5) Find any interesting trends/behaviors that you encounter when you analyze the dataset. 



### 4)Preliminary Analysis Section

#### Aboard Vs Fatalities
The box plots and distribution plots for Aboard and Fatalities columns conveyed that the maximum number of fatalities and people boarding the flight for each crash are in the range 0-100, and those which are more than 100 in number for any accident in the data set are rare.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Dist%20%26%20Box%20Plot%20for%20Fatalities.png)

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Dist%20%26%20box%20plot%20for%20aboard.png)

#### Fatalities Vs Accidents
The scatterplot is plotted for the each operator's accidents count and fatalities from all of its accidents, the observation obtained is as follows:
Maximum number of operators are crashed in the range of 0 - 50 accidents where the maximum fatalities for an accident are in the range 0 - 1000

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Scatter%20plot%20for%20Accident%20vs%20Fatalities.png)

#### Bar Graph for fatalities per each accident for airlines with >10 accidents 
Bar graph is plotted for fatalities on each accident for every airline. The fatalities observed for each accident are in the range of 0 - 60 and When the number of accidents are considered for every airline, the Aeroflot and Military - U.S. Air Force are having the highest number of accidents, which is >175.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Fatalities%20Per%20Accident.png)


#### Accident Trends
Accidents gradually increased over 1908 to 1970 and there is gradual decrease in flight accidents till today. while comparing the fatalities and accidents, the interesting scenario which was observed in the below graphs is the ratio of fatalities to accidents is equally distributed in both the graphs except during the time period 1940 - 1960, the number of fatalities are less compared to the number of accidents in that period of time.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Accidents%20per%20Year.png)

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Fatalities%20per%20Year.png)


Also, the number of accidents are high in December and January compared to other months and during the weekday’s numbers are high compared to weekends, specifically on Tuesday and Thursday.
The below graph represents that the very peak time of accidents, which is during 3PM and other times are comparatively very low. Also, highest trends are for Aeroflot and US Military operators.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Accidents%20by%20Month%2C%20Day%20%26%20Hour.png)

The flight trends for different operators can be seen below. The max and highest is for Aeroflot.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Fatality%2C%20Accident%20trend%20by%20Operator.png)

The survival rate is drastically improved compared to 1908 and 2020 as seen below.

![](https://github.com/sandeepreddyb253/CMPE255-AirplaneCrash/blob/main/Images/Average%20survival%20rate%20per%20year.png)

The topflight crashes have happened by operator Aeroflot and in Location Sao Paulo, Brazil.

##### The following causes have been identified for Top 5 crashes:

1: Spatial disorientation due to bad weather conditions.

2: Stalled the engine. The explosion or destruction of the aircraft from falling to the ground or collision with the building.

3: Failure of the rotor or problems with the fuselage (specifically problems with the tail). It is also a possible mistake of the Air Traffic Control center.

4: Bad weather conditions: strong wind, snow, ice. The plane disappeared from radar.

5: Taking off without clearance from ATC. ATC or pilots’ error.


### Two Methods

1.	K-Means Clustering: Clustering will be applied for Summary feature using TF-IDF numerical statistic to classify groups of crashes.
2.	Random Forest: Dimension reduction will be performed, and top 5 features will be extracted, and these attributes will be considered to perform prediction for higher accuracy.


