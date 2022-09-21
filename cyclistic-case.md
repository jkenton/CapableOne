---
title: "Cyclistic Bike Share Case Study"
layout: page
permalink: /data/cyclistic/
---


### Ask

The task is to

1. analyze the data to find relevant ways that casual users differ from members

2. formulate a strategy to attract casual users to consider joining as members

  

### METHOD

  

The data I analyzed to visualize these relevant differences came from the Cyclistic Bike Share data repository. I downloaded all data from September 2021 to August 2022 inclusive. This consisted of 12 zip files, each containing one month's worth of ridership data.

I extracted the zip files to a local computer, and made archive copies of the original CSV files.  

I then loaded the files into Microsoft Excel and familiarized myself with the data. To assist data analysis, I created two new columns. One was created to provide information about ride duration, the other was created to identify the day of the week for each of the rides.

After seeing that the data problem only affected location-to-location trends, and not riedership information, I elected to remove columns that had location-related data to simplify the analysis materials. The concerns section has more detail about this decision.

I assured that each of the thus-reduced data files had all pertinent data for the ridership questions. There were no missing values across the twelve data files. There was information about all 5,883,043 ride segments.

I completed a pivot table analysis of the data, using casual-member as the row information, day-of-the-week as column information, and values came from the count of rides, and the average duration of rides.

From this information, a summary table was created, showing monthly break-downs of daily average ride length and number of rides for both members and casual riders.

The summary table was used to create some visualizations that helped to identify important differences between members and casual users. What follows is an annotated graphic summary of the data files, with interpretation that may become useful for marketing purposes.

#### CONCERNS

I noted that many of the data records were missing information related to starting GPS location, ending GPS location, and also many were missing data related to the station where the bikes were originally rented, and where they were returned. Since the question was only concerned with differences in patterns of use volume, rather than more qualititative concerns (like which depot would benefit from having more bikes available on given days), I made copies of the data files, and omitted the columns related to starting and ending locations and stations from the data files that generated the visualizations above.

If a future analysis is undertaken regarding the begin- and end-points of the ride segments, a method must be created to deal with this substantial volume of missing data.

Another significant concern with the data was a substantial drop noted in the May data set related to casual Thursday bikers.

### RESULTS

One fairly clear difference between casual and member riders was seen in the difference of average ride duration. Whereas the members were fairly consistent in their average usage as a group (12 mins and 29 seconds, plus or minus two minutes), casual riders made longer rides on average (28 mins and 40 seconds, plus or minus four minutes). This difference was consistent for every month. (Casual rides are shown in red, member rides are shown in blue)

[image:casual_longer_rides.png]

Another difference between the two groups was in number of rides. Members used the system far more frequently than casual users. One additional insight in the graphic is that the overall rate of ridership declines between the months of November and April, which coincides with Winter in Chicago. (Casual rides are shown in red, member rides are shown in blue.)

[image: casual_more_rides]
  
These insights alone are not particularly useful, so I dug a little deeper to see whether there were weekday-weekend differences in addition to these monthly trends.

#### Weekday differences
This graphic shows that there are far more member riders on weekdays, when compared to casual riders. For this analysis, Weekdays were considered Monday through Thursday. With only very rare exceptions in May and June, the number of member riders clearly exceeds casual riders. To make the distinction more clear, the causal rider information is rendered in color, while the member rider information is in gray. 

[image:weekday_rides]

Continuing the trend, this graphic shows that casual riders use the bikers far longer per ride when compared to members.

[image: weekday_duration]

#### Weekend Differences

A number of differences appear when the weekend days are separated from the weekdays. For this analysis, weekend days were Friday, Saturday, and Sunday.

The number of casual rides exceeds the member rides on Saturday and Sunday in the months of May, June, July, and September. The number of casual rides on Saturday also exceeds member rides in August. To make the distinction more clear, the causal rider information is rendered in color, while the member rider information is in gray.

[image: weekend_rides.png]

Weekend casual rides continue to be longer than weekend member rides. The member ride information is rendered in gray, and the casual ride information is in color. To help make the distinction more clear, an average casual duration line is included in dark red, and an average member duration line is included in dark blue.

[image: weekend_duration.png]

#### Summary



### Recommendations

<figure>
 <img src="/images/EDIT ME" alt="EDIT ME">
 <figcaption>EDIT ME</figcaption>
</figure>
