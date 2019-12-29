# Ford GoBike System Data Exploration
### by Karan Bhardwaj


## Dataset

This is data of 4554806 rides of Ford GoBike System data starting from June 2017 until October 2019. 
Most variables are categorical except the duration_sec which is duartion of each ride in seconds. 
We also have two timestamp variables of when the ride start i.e. start_time and end_time i.e. when the ride ended.
I am interested in following points:- 
- Ride duration spread of the dataset.
- Avg Ride Duration of a trip. 
- When are most trips taken in terms of time of day, day of the week, or month of the year?
- Does above are impacted by User Type i.e. user being a subscriver or a customer. 
I have created following fields to analyse dataset in more depth: - 
- start_time_hour :- Hour of start time of the ride
- start_time_month :- Month of start time of the ride
- start_time_year :- Year of start time of the ride
- start_time_weekday :- Weekday of start time of the ride 
To break down the ride by time of day, day of the week, or month of the year I have selected 
start_time as it directly relates to when the trip/ride started.

## Summary of Findings

In the exploration, I found out that ride duration has a long tail initially but after plotting on a 
logarithmic scale found out that the spread was unimodal with peak around 500-630 seconds and 
mean avg duration of 861 seconds. Majority of rides are by subscriber user type in comparison with 
customer user type. On further investigation by user type I found that the mean ride duration by user type 
varies significantly. Customer ride duration mean is 3 times of the Subscriber ride duration mean. Upon
cumulative investigation of data by time of the day, day of week and month of year and then broken by
user type the findings were similar for time of the day and day of week with few exceptions. But in case
of month of the year the initial bias of October being the month with highest rides was disqualified when
broken by year. Ride duration distribution is opposite to the count of rides distribution by user type.
Dire duration means by user type at cumulative and while broken down by time of day, day of the week, or 
month of the year suggest that Customers use bike sharing for longer durations in comparison with Subscribers.


## Key Insights for Presentation

For the presentation, I focus on just the influence for user type on ride distribution as well their
corresponding means. Both user types are unimodal in terms of their distribution. 
Afterwards, I introduce the impact of user type on count of rides and ride duration distribution. 
I use subplots to combine different charts together to be compared and insights delivered clearly. 
Next, I compare cumulative trend of count of rides by time of day and day of the week with user type trend
of the same period using subplots. I've made sure to use different color palette for different user types to deliver insights.
Lastly, I compare cumulative distribution of ride duration by time of day and day of the week with user type distribution
of the ride duartion to same period using subplots. As above I've made sure to use different color 
palette for different user types to deliver insights.
