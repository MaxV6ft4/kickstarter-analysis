# Analysis of kickstarter campaigns for Louise
In this spreadsheet, you will find that I have added into the main table a percentage of the amount funded for each campaign, the average donation of each backer, as well as the date each campaign began and ended, written in regular form.  In additional tables you will see charts explaining the outcomes of each campaign based on category, subcategory and launch date, statistical analysis on US plays, and finally a box plot showing the average goals and pledges for Great Britain's musicals.

[Max V analysis](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Max_V_kickstarter_analysis.xlsb)

## Basic analysis
In the Outcomes category I assigned a different color to correspond to each different type of outcome.  Then I created two new columns (O and P) called Percentage Funded and Average Donation, respectively.  In Percentage Funded, I divided the goal by the total amount pledged, then multiplied by 100 to show the result as a percentile.  Additionally I used conditional formatting to display successfully funded campaigns in blue and failed campaigns in red.  For successful campaigns, the lighter the blue means the amount funded went well over 100 percent.  For failed campaigns, the lighter the red means the amount funded was almost or at zero.  In Average Donation I divided the number of project backers by the total amount pledged.  Finally, I created two new columns at the very end of the table which converted the beginning and end of each launch date from unix timestamps to regular dates. 

Next I created three new tables, each with a corresponding pivot table and graph. 

The first displays the outcomes for each parent category. 

![Category Stats](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Category_Stats.png)

We can see that there are 839 total successes in theater campaigns.  Upon filtering the pivot table to show only US theater campaigns, we see that 525 of them were successful.  The UK only produced 258 successful theater campaigns.

The second table displays the outcomes for each subcategory. 

![Subcategory Stats](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Subcategory_Stats.png)

Here, plays are clearly the winner, with 694 successful campaigns, 412 of which took place in the US.  It looks like you have chosen the correct country to produce a play in.

Finally, the third table displays the outcomes for each parent category based on the launch date.  

![Outcomes Based On Launch Date](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/Outcomes_Based_On_Launch_Date.png)

May is clearly the most successful month.  June looks promising as well, but upon closer inspection we can see that the number of failed campaigns increased from May to June and stayed that way through July.  Start your campaign in May!

Based on your interest in five plays that took place at Fringe, I created a new table (Edinburgh Research) featuring the plays, their goals, amounts pledged, the number of backers and the average donation per backer.  All five campaigns were successful, and nearly each one had a total amount pledged reach just slightly over the goal, but the biggest goal was only $4,000, two-thirds less than your hopeful goal of $12,000.  The average campaign donation ranged between $33 and $52 per backer, but the real difference lies in the number of backers for each play (less backers means more money donated per backer).  Formulate your gameplan ahead of time in order to gain as many backers as possible!  Some campaigns don't last too long, either.  For example, the successful campaign for the play Walken On Sunshine had 173 backers, averaged $71.24 per donation, and lasted only for one month!

## Statistical Analysis
Since you desire to create and put on a play in the United States, I created new tables using data filtered from the Kickstarter sheet to only include successful and failed US plays, respectively.  Then I created a third table (Descriptive Statistics) containing the mean, median, standard deviation and quartiles for the campaign goals and amounts pledged.  Let's start with means and medians.

The mean (average) goal for successful campaigns is just over $5000, and the median (middle number) is $3000. However, for failed campaigns the mean lies around $10,550 and the median is $5000, both higher than the successful mean and median.  This does not fit into your $12,000 goal that well.  Furthermore, the mean total amount pledged for successful campaigns is $5600, and the median is around $3100, both very close to the mean and median goals.  But, *both the mean and median total amounts pledged for failed campaigns don't even reach $1000*.  This means that there is another factor besides money making people hesitant to back these plays.  As I mentioned before, you should have a clear vision of what you want out of your play before you begin your campaign, in case there are some backers that are on the fence about making a pledge.

There are three additional factors to consider here.  
-The standard deviation for the goals and pledges of both successsful and failed campaigns is larger than the mean.  This means that the majority of campaign goals and pledges beneath the mean lie close to the median.  
-The upper quartiles (where 75% of the data is less than the number listed there) for the goals and pledges of both successful and failed campaigns just about equal their respective means. 
-The standard deviations are all more than double the Inter-quartile ranges (the difference between the upper and lower quartile, the lower quartile being where 25% of the data is less than the number listed there).  

We can conclude from these factors that the dataset is being lead by some very, very large numbers, more specfically certain large campaign goals that have mostly failed.  Therefore I would highly recommend reducing your $12,000 goal by about 75% if you want a better chance at successfully kickstarting a play in the US.

## Analysis On Musicals In Great Britain
![GB Musicals Box Plot](https://github.com/MaxV6ft4/kickstarter-analysis/blob/main/GB_Musicals_Box_Plot.png)

Above are respective box plots on goals and amounts pledged for musicals taking place in the UK, since you have expressed interest in creating a musical there.  Here, the mean goal (where the x is located within the plot) is just around 4000GBP, which looks fine based on your 4000GBP budget, but if we look at the box plot for amounts pledged, we see that 4000GBP is well above that mean (less than 2000GBP).  I would recommend halving your budget for a UK musical, should you choose to proceed with the campaign.

# Conclusion
Staging a play in the United States is your best option for success.  Start your campaign in May, present your vision to prospective backers beforehand, and *significantly* decrease your budget.
