<h1>Analysis and comparison of casual and annual member riders of bike-sharing company<h1>

<h2>Description</h2>
<br /> This repository shows the analysis of the bike-sharing company. The RMarkdown file covers the analysis of the behavior of riders and comparison between casual users and annual member users. The necessary dataset can be found through this <a href="https://divvy-tripdata.s3.amazonaws.com/index.html">link</a>. 
<br />

<h2>Languages and Utilities Used</h2>

- <b>R </b> 
- <b>R Studio</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Analysis and Visualization walk-through:</h2>

<p align="center">
STEP-1 We start with loading required tools and setting working directory: <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz1.png"/>
<br />
<br />
STEP-2 Then we upload necessary documents from directory and name them :  <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz2.png"/>
<br />
<br />
STEP-3 Before merging them, we have to check if the names of columns are consistent :  <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz3.png"/>
<br />
<br />
STEP-4 We change the 'ride_id' and 'rideable_type' columns to character so they can stack properly: <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz4.png"/>
<br />
<br />
STEP-5 Then we upload necessary documents from directory and name them:  <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz5.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz6.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz7.png"/>
<br />
<br />
STEP-6 Finally, we start to merge individual monthly files into quarterly reports:  <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz8.png"/>
<br />
<br />
STEP-7 Now it is time to inspect the created table:  <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz9.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz10.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz11.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz12.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz13.png"/>
<br />
<h2> Then we repeat the same steps to create other quarterly reports (Summer, Fall, Winter). I am going to skip these steps but they can be found in this <a href="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_Ready_Analysis.html">html file</a> I uploaded in the repository.
<h2>
<br />
STEP-8 We can create an anuual report through combining quarterly reports:  <br/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz14.png"/>
<br />
<h1> ==== ANALYSIS ==== <h1>
<h2> Before starting there are few problems we need to fix:

<br />(1) The data can only be aggregated at the ride-level, which is too granular. We will want to add some additional columns of data – such as day, month, year – that provide additional opportunities to aggregate and analyze the data.
<br />(2) We will want to add a calculated field for length of ride to calculate how long members vs. casual riders use the bikes. We will add “ride_length” to the entire dataframe for consistency.
<br />(3) There are some rides where tripduration shows up as negative, including several hundred rides where Divvy took bikes out of circulation for Quality Control reasons. We will want to delete these rides.
<br />(4) We check if different labels are used for ‘member_casual’ column
<h2>
<br />
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz15.png"/>
<br /> Add columns that list the date, month, day, and year of each ride <br />
This will allow us to aggregate ride data for each month, day, or year … before completing these operations we could only aggregate at the ride level <br />
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz16.png"/>
<br/ >
<br/ > Add a “ride_length” calculation to all_trips (in seconds)

<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz17.png"/>
<br /> Check the structure of the data to see the changes we made so far
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz18.png"/>
<br />
We found out that ‘ride_length’ is not numeric value but factor value so we will change it to numeric to perform calculations on it
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz19.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz20.png"/>
<h1> ==== DESCRIPTIVE ANALYSIS ====
<h1>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz21.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz22.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz23.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz24.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz25.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz26.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz27.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz28.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz29.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz30.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz31.png"/>
<img src="https://github.com/miracle99shoh/bike_share_analysis/blob/main/Case_study_1_Cyclistic_viz32.png"/>






</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
