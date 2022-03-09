# PyBer Analysis
An analysis of ride-sharing data was performed from January to May 2019.  Three categories were defined based on city type: rural, subruban, urban.  The following data was calculated within each category: total drivers, total fares, average fare per ride, average fare per driver.  Further analysis was requested to have this information broken down by week from Jan 1st through April 28th (refer to "PyBer Analysis Graph" shown below).

## Results
Urban areas had the largest values for total rides (1,625), total drivers (2,405) and total fares ($39,854.38).  Suburban had the next highest with 625 for rides, 490 for drivers and $19,356.33 for fares.  Rural had the smallest values at 125 for rides, 78 for drivers and $4,327.93 for fares.  The opposite was true for average fare per ride and average fare per driver.  Rural had the highest values at $34.62 and $55.49, followed by suburban ($30.97 and $39.50) and then urban ($24.53 and $16.57).  When looking at the weekly performance from 01-01 to 04-28, the data shows a couple of trends.  Urban and suburban values are lowest in January and all three city types show a spike heading into March.

## Summary
The more populated areas show more frequent rides (resulting in more drivers and higher total fare), while the cost per ride is lower.  Rural areas have rides less frequently, but cost more per ride.  Considering that the total fare for rural areas is still very low even with the higher fare per ride, it may be beneficial to find ways to generate business more frequently (example: food delivery) in those areas.  Otherwise, even higher fare prices in those areas may be necessary.  Another suggestion would be to find incentives for more ride sharing in January for urban and suburban areas.

## References:
### Code examples:
`fare_summary_df_pivot = fare_summary_df.pivot(index="date", columns="type", values="fare")`

`fare_jan_apr_df = fare_summary_df_pivot.loc["2019-01-01":"2019-04-28"]`

`fare_weekly_df = fare_jan_apr_df.resample("W").sum()`

### Database pics:
![PyBer Analysis Graph](https://github.com/tonyferri/PyBer_Analysis/blob/main/Analysis/PyBer_fare_summary.png)