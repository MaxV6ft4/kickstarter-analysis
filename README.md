# Kickstarter Analysis for Louise

## Project Overview
Based on previous analysis, I was able to help guide Louise towards successfully launching a funding campaign for her play, *Fever*.  This time I will be conducting analysis on other campaigns to show Louise how they compare to her own.

### Purpose
I have added two new sheets to the workbook to describe to Louise how different kickstarter campaigns have performed in relation to their launch dates as well as to their funding goals.

## Analysis and Challenges

[Kickstarter Analysis](http://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Kickstarter_Challenge_copy.xlsx)

### Analysis of Outcomes Based on Launch Date
I first created a Years column in the original Kickstarter sheet (column U).  This column displays the year of the date each campaign began.  Next, I created a new sheet and called it 'Theater Outcomes By Launch Date'.  I then inserted a pivot table displaying the total number of outcomes, separating them into successful, failed and canceled columns; rows were arranged to display months.  Then I created filters for both the parent category (so we can see the results strictly for the theater) and years.  Finally I created a line graph with markers, displaying the trajectories for successful, failed and canceled campaigns per month.  

![Theater Outcomes Based on Launch Date](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
I created a second new sheet, called 'Outcomes Based On Goals', and added eight columns.  The first column displays the funding goals for each play.  In each row the goal amount increases, starting from less than $1000 and ending with greater than $50,000.  In order to calculate the number of successful, failed and canceled plays I used the COUNTIFS function by collecting data from three columns in the Kickstarter sheet: outcomes (minus live ones), goals, and subcategories (filtered to only show plays). These results are displayed in columns B through D.  In column E I added the total number of successful, failed and canceled plays in each row.  In columns F through H, I calculated the percentage of success, failure and cancelation using the ROUND function.  I divided the number of successful, failed and canceled campaigns, respectively, by the total number of projects in each goal range.  I then changed the format in those columns to display the result as a percentage.  For example, in row 2 I divided the number of successful plays with a goal under $1000 (141) by the total number of plays in that goal range (186) to get a success rate of 76%.  Finally I created a line graph displaying the percentage of successful/failed/canceled plays in relation to their goal range.

![Outcomes Based on Goals](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
When creating the 'Outcomes Based on Goal' sheet, I had a problem calculating the percentages using the ROUND function at first.  The result always displayed a whole number but when I changed the format to percentage the number would always add two zeros.  Furthermore, the graph would not display a percentage next to the number on the y-axis.  To fix this, I made two tweaks to the ROUND function.  I added a '2' instead of a '0' at the end of the function so it would display two decimal places instead of zero, plus I removed the x100 input so I could manually change the number to a percentage afterwards.  This way, the numbers showed up on the graph's y-axis as a percentage.  

## Results
When comparing theater outcomes to their launch date, we can see in the graph that May is clearly most successful month to launch a kickstarter (there were 40 more successful theater launches in May than in April).  However, failed launches go up in May as well and only slightly go down in June, remaining mostly stagnant through August.  Furthermore, the line of failed outcomes exhibits a similar trajectory to the line of successful outcomes throughout the entire year, with the exception of May.  All signs point to May for a more successful campaign launch!

When comparing play outcomes to their campaign goals, we notice that campaigns are most successful when their goals are less than $1000 and are least successful when their goals are between $45,000-$49,999.  The inverse is true for failed campaigns.  They failed the most when their goals were between $45,000-$49,999 and failed the least when their goals were under $1000.  In fact, the entire failed line is the inverse of the entire successful line.

There are a couple limitations in this dataset to consider:

-in the 'Outcomes Based on Goals' sheet, the number of successful and failed plays both drop significantly when the goal exceeds $14,999.  The graph displays a low percentage of successful outcomes and a high percentage of failed outcomes using a very limited amount of data.  
-there are no canceled *plays* in the dataset (only canceled theater campaigns, and even those are scarce).  This could be interpreted as either not enough data was collected or simply that once a campaign started, it either succeeded or failed.

Lastly, I would recommend another graph be created in 'Outcomes Based On Goals' to display the *number* of plays on the y-axis instead of the percentage to get a more detailed picture of outcomes per goal, given the limited amount of data.
