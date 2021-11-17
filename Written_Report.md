# Kickstarting with Excel

## Overview of Project

### Background
One of Louise's plays completed its fundrasising goals pretty quickly. This made Louise think how different campaigns performed with respect to their start dates and funding goals and how many of them completed their goals. 

### Purpose
The purpose of the analysis is to figure out how does the start date for a campaign afect its chances of success. Also, the analysis tries to answer the question if plays funded by a specific amount of money have greater chances of success or failure than others.

## Analysis and Challenges

### Analysis
The analysis for this problem is broken down in two parts:

1. Analysis of Outcomes Based on Launch Date
2. Analysis of Outcomes Based on Goals
 
#### Analysis of Outcomes Based on Launch Date
The first part of the analyis was to figure how the starting month of a campaign influences the the success chances of a campaign.

The analysis involved creating a pivot table out of the main Kickstarter campaign to better understand how the starting month of a campaign is related to the overall success of a campaign. In order to achieve this, I created a pivot table using the following columns from the spreadsheet:
- Parent Category
- Years
- Outcomes
- Date Created Conversion

Since we are only interested in theaters, the Parent Category was selected as a filter. The Years column was also added as a filter to look at how similar months/time period in different years affected the chances of succes of a play.

The pivot table gives a concise picture of the raw data and helps to understand the effect of starting months on a campaign.

![Pivot_table_Outcome_Months](https://github.com/abhi82git/kickstarter-analysis1/blob/512ac5d95ac33fa17a907a909a4070d575018f62/Pivot_Putcomes_Months.png)

#### Analysis of Outcomes Based on Goals
The second part of the analyis was to figure how the goal amount for a campaign influences the the success chances of a campaign.

The first part of the analysis was to break down the goal amounts into logical groupings to compare the effect of goal amounts. While it is always better to have smaller groups, since that allows more granularity to analysis, it is also important to have a big picture overview which can be lost in too small groupings. Hence, the decision was made to split the goal amounts in 10 equal partitions apart from lowest and biggest amounts.

After creating the groups, the next task was to count the number of Succssful/Canceled/Failed campaigns for each subgroup. In order to achieve this, the COUNTIFS function was used to calculate the number of succssful/failed/canceled campaigns for each subgroup. The COUNTIFS function allows the user to filter on multiple values in one shot. From the individual counts, the total projects for each subgroup was arrived at. This allowed to calucalte the percentage of suuccesful/failed/canceled campaigns. 

![Analysis_Outcome_Goals](https://github.com/abhi82git/kickstarter-analysis1/blob/2d51fadb4ce99f2d352fd41b05c5046cf5bb77a1/Analysis_Outcomes_Goals.png)

### Challenges and Difficulties Encountered

#### Challenges
**Deliverable 1**
The main challenge in this activity was to fugure out how to display the counts against months. Upon drgagging *Date Created Conversion* under Rows in the pivot table, you get the time period broken down in years by default.

![Time_Period_Years](https://github.com/abhi82git/kickstarter-analysis1/blob/6ef48c9f5e61281b3b66e4081b991bcfa90d2d48/Time_Period_Years.png)

Upon looking carefully, I noticed that te dragdown of *Date Created Conversion* also resulted in two extra fields under rows:
  - Years2
  - Quarters

![Pivot_Table_Rows_Time_Period](https://github.com/abhi82git/kickstarter-analysis1/blob/6ef48c9f5e61281b3b66e4081b991bcfa90d2d48/Pivot_Table_Rows_Time_Period.png)

Upon removing *Years2* and *Quarters* fields from under the Rows field, I was able to get the data just for months.

![Pivot_Table_Rows_Time_Period_Months](https://github.com/abhi82git/kickstarter-analysis1/blob/6ef48c9f5e61281b3b66e4081b991bcfa90d2d48/Pivot_Table_Rows_Time_Period_Months.png)


**Deliverable 2**
The challenge in this deliverable was the use of COUNTIFS function, since I haven't used it in the past. I overcame the issue by searching for the syntax and use of COUNTIFS function and was able to figure it out.


**Other Challenge**
The other biggest challenge was to write this report in git (.md) format in a way that is readable on git, since this is my first time using GIT. In fact, it took me more time to figure out the formatting/structuring than it took me to complete the assignment. I used the [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#uploading-assets) to learn the structure and write the report.


## Results

### Conclusions from Outcomes based on Launch Date

 - The month of **May** saw the most successful and failed campaigns.
 - Campaigns were either successful or they failed. The number of theater campaigns that were canceled was very small.
 
![Theater_Outcomes_vs_Launch](https://github.com/abhi82git/kickstarter-analysis1/blob/2fcb36b1ec6df8bfa5e22bb3bedd0d9d5003015c/Theater_Outcomes_vs_Launch.png)

### Conclusion from Outcomes based on Goals
- The percentage of successful campaigns was the highest at lower goal values, which is pretty obvious since it is a smaller goal to achieve. What's interesting though is that the percentage gradually starts going down as goals increase till they start rising again and reach highs at $35,000 to $45,000. The failure rate of campaigns again goes up with higher goal amounts. 

![Theater_Outcomes_vs_Goals](https://github.com/abhi82git/kickstarter-analysis1/blob/2fcb36b1ec6df8bfa5e22bb3bedd0d9d5003015c/Outcomes_vs_Goals.png)

## Limitations

## Other Possible Takes
