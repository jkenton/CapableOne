---
title: "Case Study"
layout: page
permalink: /data/cyclistic-case/
---

# Cyclistic Bike Share Case Study

## Task

The task is to

1. analyze the data to find relevant ways that casual users differ from members

2. formulate a strategy to attract casual users to consider joining as members

  

## METHOD
 

The data I analyzed to visualize these relevant differences came from the Cyclistic Bike Share data repository. I downloaded all data from September 2021 to August 2022 inclusive. This consisted of 12 zip files, each containing one month's worth of ridership data.

I extracted the zip files to a local computer, and made archive copies of the original CSV files.  

I then loaded the files into Microsoft Excel and familiarized myself with the data. The data sets each contained columns for unique ride ID, type of bike, start time, end time, start location, end location, ridership (member or casual) and then a GPS coordinate for start location and end location. To assist data analysis, I created two new columns. One was created to provide information about ride duration, the other was created to identify the day of the week for each of the rides.

While investigating the data sets, the columns devoted to start location and end location had an exceptional number of missing values. After verifying that the data problem was worst for location-to-location trends, and not rideership information, I elected to remove columns that had location-related data to simplify the analysis materials. The concerns footnote has more detail about this decision.[^1] The trimmed data contained seven columns: ride ID, bike type, start time, end time, member/casual, ride duration, and the day of the week.

The 12 data sets were then loaded into RStudio for further analysis. To this data, I loaded libraries for tidyverse, dplyr, chron, and lubridate. Chron and lubridate were necessary to deal with the time-based values stored in the ride duration column.

The descriptive table below shows the number of rides purchased in a given time frame, and the number of those rides taken by members, or by casual riders.

## RESULTS

---

### DESCRIPTIVE INFORMATION

|Segment |Total Rides | Members | Casual|
|---|---|---|---|
|September|756147|392257|363890|
|October|631226|373984|257242|
|November|359978|253049|106929|
|December|247540|177802|69738|
|January|103770|85250|18520|
|February|115609|94193|21416|
|March|284042|194160|89882|
|April|371249|244832|126417|
|May|634858|354443|280415|
|June|769204|400153|369051|
|July|823488|417433|406055|
|Aug|785932|427008|358924|
|**Annual**| **5883043**|**3414564**|**2468479**|

Interpretation: The table shows that the months of June through September each had more than 700,000 rides, and that the months of December through March each had less than 300,000 rides. Higher numbers of rides coincide with the summer (warm-weather) months, and lower numbers coincide with winter (cold-weather) months.


[^1]: I noted that many of the data records were missing information related to starting GPS location, ending GPS location, and also many were missing data related to the station where the bikes were originally rented, and where they were returned. Since the question was only concerned with differences in patterns of use volume, rather than more qualititative concerns (like which depot would benefit from having more bikes available on given days), I made copies of the data files, and omitted the columns related to starting and ending locations and stations from the data files that generated the visualizations above.<br>If a future analysis is undertaken regarding the begin- and end-points of the ride segments, a method must be created to deal with this substantial volume of missing data.

---

### Annualized Data
Figure 1 shows the Annual summary of rides, broken down by membership status (member v. casual)

Figure 1:<br/>
<img src="/images/ann_summ_num.png" alt="This image shows the annual summary of rides by day of the week">

The graphic shows that the members vary between 400,000 and 550,000. The membership curve has an inverted-U shape, with low numbers on Saturday and Sunday, and highest numbers on Wednesday. The casual rider curve is almost the opposite. The casual rider curve is a U-shape, and ride numbers varied between 275,000 to 510,000, with low point on Tuesday, and high points on Saturday and Sunday.

There are two additional ways to visualize this annual data. One is by bike type ridden (classic, electric, or docked), and the other is by ride duration. Figure 2 shows the annual ride data summarized by bike type. Figure 3 shows the annual summary of ride duration by bike type and membership.

Figure 2: <br/>
<img src="/images/ann_summ_bike_type.png" alt="This image shows the annual summary of rides by bike type">

Interpretation: There are two principal types of bikes, classic and electric. During weekdays, there is no substantial preference between the two types. On weekends, there does seem to be a preference for classic bikes over electric. One thing to note is that "docked bikes" were only used by casual riders. The use od docked bikes showed similar trends with typical casual rider behavior with maximum use on weekends and a U-shaped curve during the week, with a low point on Wednesday.

Figure 3:<br/>
<img src="/images/ann_summ_duration_bike_member.png" alt="This image shows the annual summary of ride duration bike type, membership, and by day of the week">

Interpretation: The usage trends are clear on a yearly scale. Docked bike rides are substantially longer (though they account for the fewest number of rides as shown in Figure 2) than any other use. In descending order, casual classic and electric bike rides showed longer durations than member rides. Casual rides also had a similar U-shape to the number of rides, with shortest rides in midweek, and longer rides on weekends. Member rides seemed very consistent in duration, with classic bikes being used more often than electric. 

One may make the assumption that casual riders use the bikes in different ways when compared to members. Whereas members may use their bikes along consistent routes, with consistent start and end points, casual riders may tend to use the bikes for exploration or open-ended purposes.

Figure 4 shows the overall summary of bike type, membership, and day of the week.

Figure 4:<br/>
<img src="/images/ann_summ_bike_member_day_of_week.png" alt="This image shows the annual summary of membership, bike type, and day of the week">

Interpretation: Whereas members maintained their preference for classic bikes throughout the week, casual riders preferred electric bikes during the week, and were equally interested in classic and electric bikes on weekends.

---

### Seasonal Data

For the analysis, the data were grouped into four seasonal blocs: July, August, and September were grouped as "Summer"; October, November, and December were grouped as "Autumn"; January, February, and March were grouped as 
"Winter", and; April, May, and June were grouped as "Spring."

---

#### Autumn

Figures 5, 6, 7, and 8 will show the same segmentation of the data as the annualized Figures 1-4.

Figure 5:<br/>
<img src="/images/aut_summ_num.png" alt="This image shows the Autumn summary of rides by day of the week">


Interpretation: Total number of member rides is greater that casual rides across all days of the week. Trends continue, with number of member rides higher in midweek than on weekends. Likewise, and in opposition to the member rides, casual rides have their highest values on weekends, and lowest during the week.

Figure 6:<br/>
<img src="/images/aut_summ_bike_type.png" alt="This image shows the Autumn summary of rides by bike type">

Interpretation: The bike type data begins to show a preference for electric bikes every weekday, and closer to parity with classic bikes on weekends.

Figure 7:<br/>
<img src="/images/aut_summ_duration_bike_member.png" alt="This image shows the Autumn summary of ride duration bike type, membership, and by day of the week">

Interpretation: The ranking of duration by membership and by bike type is very similar to Figure 3, with docked, casual-classic, casual-electric, member-classic, and member-electric in descending rank order.

Figure 8:<br/>
<img src="/images/aut_summ_bike_member_day_of_week.png" alt="This image shows the Autumn summary of membership, bike type, and day of the week">

Interpretation: Members continue to favor classic bikes over electric, though there was parity between electric and classic bikes on Thursdays and Fridays. Casual riders clearly favored electric bikes each day, and docked bike usage continued the same U-shape curve, with greater use on weekends and far less on weekdays.


---

#### Winter
Figures 9, 10, 11, and 12 will show the same segmentation of the data as the annualized Figures 1-4.

Figure 9:<br/>
<img src="/images/win_summ_num.png" alt="This image shows the Winter summary of rides by day of the week">

Interpretation: In winter, member ridership continues its inverted-U shape trend; with ~40,000 rides each weekend day and ~60,000 on weekdays. Casual ridership falls off substantially. Casual ridership is consistent between 12,000 and 23,000 rides

Figure 10:<br/>
<img src="/images/win_summ_bike_type.png" alt="This image shows the Winter summary of rides by bike type">

Interpretation: There is more parity across the winter season between electric and classic bikes.

Figure 11:<br/>
<img src="/images/win_summ_duration_bike_member.png" alt="This image shows the Winter summary of ride duration bike type, membership, and by day of the week">

Interpretation: Similar to other trend graphics, usage is in descending order: docked, casual-classic, casual-electric, member-classic, member-electric.

Figure 12:<br/>
<img src="/images/win_summ_bike_member_day_of_week.png" alt="This image shows the Winter summary of membership, bike type, and day of the week">

Interpretation: Figure 12 shows that members continue to prefer classic bikes over electric. The usage trends for casual look virtually the same for everyday of the week, continuing the casual rider preference for electric bikes over classic.

---

#### Spring
Figures 13, 14, 15, and 16 will show the same segmentation of the data as the annualized Figures 1-4.

Figure 13:<br/>
<img src="/images/spr_summ_num.png" alt="This image shows the Spring summary of rides by day of the week">

Interpretation: Figure 13 shows that casual ridership exceeds member ridership on weekends, and has substantially rebounded from Winter numbers on other days of the week. Similar to other seasons, member ridership shows the inverted-U shape trend with highest ridership mid week, and lower on weekends.

Figure 14:<br/>
<img src="/images/spr_summ_bike_type.png" alt="This image shows the Spring summary of rides by bike type">

Interpretation: There is a clear preference for classic bikes in the Spring. Overall number of rides remains consistent across weekdays and weekends.

Figure 15:<br/>
<img src="/images/spr_summ_duration_bike_member.png" alt="This image shows the Spring summary of ride duration bike type, membership, and by day of the week">

Interpretation: Similar to other trend graphics, usage is in descending order: docked, casual-classic, casual-electric, member-classic, member-electric. Across the board, each type of ride (on average) is longer than in Winter.

Figure 16:<br/>
<img src="/images/spr_summ_bike_member_day_of_week.png" alt="This image shows the Spring summary of membership, bike type, and day of the week">

Interpretation: Members continue to favor classic bikes over electric. Casual riders favored electric bikes during the week, and were at parity on weekends.

---
#### Summer

Figures 17, 18, 19, and 20 will show the same segmentation of the data as the annualized Figures 1-4. Summer has > 40% of all rides in the system.

Figure 17:<br/>
<img src="/images/sum_summ_num.png" alt="This image shows the Summer summary of rides by day of the week">

Interpretation: In summer, the number of casual rides far outnumbers member rides on weekends. Member rides continue the familiar inverted-U shape across all seven days, with higher ride numbers mid week and lowest on weekends.

Figure 18:<br/>
<img src="/images/sum_summ_bike_type.png" alt="This image shows the Summer summary of rides by bike type">

Interpretation: Across the board, classic bikes are favored over electric. This may indicate that there are fewer electric bikes, given the substantial general increase in ridership numbers.

Figure 19:<br/>
<img src="/images/sum_summ_duration_bike_member.png" alt="This image shows the Summer summary of ride duration bike type, membership, and by day of the week">

Interpretation: In this area, usage trends are the same as every other grouping. Usage is in descending order: docked, casual-classic, casual-electric, member-classic, member-electric. Across the board, each type of ride (on average) is longer than in Winter.


Figure 20:<br/>
<img src="/images/sum_summ_bike_member_day_of_week.png" alt="This image shows the Summer summary of membership, bike type, and day of the week">

Interpretation: Members continue to favor classic bikes over electric. Casual riders favored electric bikes during the week, and were at parity on weekends.

---

### DISCUSSION
There are several common themes within this data:
1. Casual users - on average - use their bikes longer than member users. Docked users (who are all casual users) use their bikes - on average - twice as long as casual users.
2. Casual users tend to outnumber member users on weekends, except during the Winter. 
3. Casual users tend to choose electric bikes more often than classic bikes
4. Summer has the highest number of rides across all seasons (Summer accounts for 40.2% of all rides); Winter has the lowest number of rides across all seasons (Winter accounts for 8.5% of all rides)


---

### RECOMMENDATIONS

The business goal is to attract more casual riders to become members. There are several sources of important differences between casual and member riders, to allow a marketing message to be targeted narrowly to casual users. 

1. Any rider who uses their bike more than 20 minutes, whether weekday or weekend, is likely to be a casual rider 

2. Any rider on Saturday or Sunday, between the months of March and August, because these are the months when casual riders outnumber members on weekends

3. Any rider checking out a "docked" bike. On average, these rides last far longer than typical casual rides

4. Casual riders are more likely than other riders to rent electric bikes

---

Recruitment ideas to try, for riders who are targeted as "casual" riders.

1. On targeted riders' checkout acknowledgement, include a link to the membership information
2. create banners to fly at stations between March and August (if start- and end-point data were available, it might be possible to target stations that have the highest frequency of casual ridership)
3. For "docked" bike riders with a very long rental, offer to roll the cost of the current rental into that month's membership cost
4. Anybody who rents a casual bike more than twice a week could receive an offer to join, showing how infrequent rentals may also be more economical under membership
4. The billing system knows which riders are casual and which are members.  Incentives to become members can be offered to ALL casual riders at check-in time.

---