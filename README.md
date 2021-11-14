# CitiBike Data Analysis

This week's project is focused on the analysis of bike sharing data. Specifically, we are working on CitiBike NYC Data to see how this business model can be applied and implemented in Des Moines (Iowa). 
The study includes the analysis of data from August 2019 since the summer months tend to have more traffic.

## Overview of the Analysis

In order to convince investors that the bike sharing program in Des Moines is a solid bussiness, we need to make a bike trip analysis and present it in a compelling way. To do so, we use `Tableau Public` and data from the Citi Bike System Data page.  

## Results

The first step in our analysis is pre-process the original data such that the information has the correct datatype.  We use Pandas to change the datatype of the **tripduration** column from an integer to a datetime datatype so we can get the time in hours and minutes.  
Once the datatype is changed, the DataFrame as a CSV file is exported to be used in the visualizations in the next part of the analysis. The Jupyter Notebook file is shown in [here](https://raw.githubusercontent.com/LeidyDoradoM/bikesharing/NYC_Citibike_Challenge.ipynb) and the visualizations created for the analysis are shown below.

1. Trips by Customer Type

The first interesting information of our analysis is related to the kind of customer that uses the bike service program.  We already know that the total rides in the month of August is *2,344,224*. Now we want to explore the types of customers and what is the proportion of short-term customers to the annual subscribers:

![CustomerType](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/CustomerType.png)

Figure 1. Customer Type Pie-chart

Approximately the 81% of the rides in the month of August corresponds to subscribers. Most of the users of the program are people that need to go around NYC in a daily basis, possibly people that live or work in the City.  Since Des Moines is a capital city with great places to live and work, there is a potential market that could use the bike service program.

2. August Peak hours:

We now want to know the peak usage hours so we can get a better idea of how many bikes we might need in Des Moines, as well as figure out during which parts of the day we will need the most bikes:

![tripPeaks](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/AugustPeakHour.png)

Figure 2. August Peak Hour bar-chart.

As it was expected, the peak hours of bycicle usage coincide with the typical rush hours, around 8 am and 5 pm. This is explained since most of the customers are anual subscribers, who probably work in the City.

3. Checkout times:

Another interesting information we can analyze is the length of time that bikes are checked out for all riders. Figure 3 shows how all of the trips last less than 1 hour. In fact, the peak of ride-lasting time is around *15* minutes.

![Checkout](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/CheckoutTimes.png)

Figure 3. Checkout Times for Users line-chart.

As an extension of this analysis, it is interesting to see how this ride-lasting information could be breakdown by Gender.

4. Checkout times by Gender:

The length of time that bikes are checked out for each gender is shown below.

![CheckoutG](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/CheckoutTimesGender.png)

Figure 4. Checkout Times by Gender line-chart.

As it can be seen in figure 4, most of the users are males.

5. Trips by Weekday:

Our analysis and plots have shown that most of the users of the bike sharing program are males probably working around NYC.  We now want to see how the number of bike trips vary by weekday for each hour of the day. The heatmap shown below display this relationship:

![Checkout](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/TripsbyWeekday.png)

Figure 5. Trips by Weekday Heatmap.

There are two different patterns: one for days of the week and other for the weekend days.  As it was expected, the week days show peak hours around 8 a.m. and 5-6 p.m, however, for Saturday and Sunday there are blocks of hours of about 7-8 hours each day that have a high volume of trips.

6. Trips by Weekday by Gender:

In order to go deep in the analysis of the previous results, we break down the number of bike trips by gender for each hour of each day of the week. Below it is the corresponding heatmap:

![Checkout](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/TripsbyGender.png)

Figure 6. Trips by Gender Heatmap.

Female and male patterns in the heatmap follow the same trend shown in figures 4 and 5. Because most of the users are males, the heatmap for males show a pattern more defined.

7. User Trips by Weekday by Gender:

Finally, we want to see how the number of bike trips are broken down by gender for each day of the week and by each User type. Figure 7 shows the corresponding heatmap.

![Checkout](https://raw.githubusercontent.com/LeidyDoradoM/bikeSharing/main/Images/UserTripsbyGender.png)
Figure 7. Trips by Usertype and Gender Heatmap.

As it was expected Customer Usertypes do not show any peak hours of bike usage. On the contrary, for subscribers, and specifically for male-subscribers, there are more use of bikes for every day of the week with respect to the female and unknown subscribers.

The complete story showing each one of the plots shown in this analysis can be seen in [CitiBike story](https://public.tableau.com/app/profile/leidy3788/viz/CitiBikeStory_16366638148210/CitiBikeStory).

## Summary

Our analysis of the NYC Citibike Data shows how most of the users of the program are subscribers, which leads us to think that the citibike users are generally people that live or work in NYC (people that need to go from one place to another place in a daily basis).  This pattern coincides with the behaviour reflected in the other plots shown in this analysis.  For example, the peak hours barchart shows how the bike-usage peak is around the traffic rush hours (8-9 a.m. and 5-6 p.m.) which at the same time coincides with the working starting and ending hours. Our analysis also shows that most of the users are male and that the average duration of the trips is around 15-20 minutes.

For further analysis, it would be interesting to see: 
- The locations around the city that have more bike-traffic.  This would help us to find areas where more bike stations are needed and also to decide the amount of bicycles needed in each station.  
- Another interesting plot could be the number of trips by age of the users, this can help to understand in more detail the type of customer that is interested in the bike-sharing program. 

