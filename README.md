# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of this project is to help a client, Louise, to evaluate ideal timing and optimal goal threshold for a Kickstarter campaign for her play. Using a data set that contains Kickstarter campaign detail spanning from 2009 to 2017, for a variety of categories and subcategories, I sought to understand which subsets and visualizations were most relevant to Louise and her play.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To help determine ideal campaign timing, I created a pivot table and chart based on the full data set. Since Louise is interested in obtaining funding for a play (a subcategory of "theater"), I used "parent category" as one of the pivot filters and selected only "theater" category data. I considered only closed campaigns (i.e. not "live") and set up the pivot table to count outcomes by month.

![Launch Date Chart](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

To help determine the ideal campaign goal, I set up a table in a new tab. I used the rows to establish 12 goal ranges, from "less than 1,000" to "greater than 50,000". For the columns in the table, I wanted to count the outcomes by type (successful, failed, canceled), and determine the percentage of each within each goal range. I then used COUNTIFS formulas to specify my criteria to obtain counts from the main data set (outcome, goal range, subcategory "plays"). I summed each outcome column and then used COUNTIFS at the bottom to check my totals against the full data set - to help validate the ranges were set up correctly in my formulas above. I then calculated row totals, and outcome percentages for each row. Finally, I created a chart from the table, using outcome percentages on the y-axis and goal ranges on the x-axis. There are 3 lines, 1 for each outcome type.

![Goal Range Chart](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

I'm familiar with Excel and most of the work performed in this project, so I didn't encounter too many issues. One challenge I encountered related to the COUNTIFS formula described in the "based on goals" analysis. I had not previously entered value ranges in COUNTIFS formulas like this, so I didn't know I needed to use quotation marks until I watched the hint video. If I were doing something like this on my own, I would have input the ranges using a numbers format versus the text/general format that we used. That way I could make them formula driven and drag them down without having to manually enter each range.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. For the "theater" parent category, it seems that May is an ideal time to launch the Kickstarter campaign. For the data evaluated, 12% of theater campaigns were launched in the month of May, and 67% of those were successful. The next closest is June, for which 65% of the campaigns were successful. This is immediately apparent when looking at the chart as well.

2. May and June are also the most popular times to launch theater campaigns in the Kickstarter data that we evaluated. 23% of theater campaigns launched in these 2 months. November and December are the least popular times to launch a theater Kickstarter campaign.

3. When considering all years together, there was never a month where there were more failed theater campaigns than successful theater campaigns, although December comes close. This trend doesn't always hold when considering individual years - for instance, 2014 and 2015 had a few months where failed campaigns exceeded successful theater campaigns.

- What can you conclude about the Outcomes based on Goals?

The most successful Kickstarter campaigns for plays occurred in the "less than 1,000" and "1,000 to 4,999" goal ranges. These are also the ranges for which most play campaigns were launched - 69% of all play campaigns were launched in these goal ranges. There has also been some success in the "35,000 to 39,999" and "40,000 to 44,999" ranges. However, there were only 9 play campaigns launched in these ranges (1% of total play campaigns), so it's potentially riskier to rely on those outcome percentages.

- What are some limitations of this dataset?

1. Potential inconsistency in currency: We have our "goal" and "pledged" amounts formatted as USD. However, given the presence of the "country" and "currency" columns, I would want to validate that all amounts are stated in a consistent currency. If not, evaluating things like outcomes based on goals could be problematic. For instance, if one goal was listed in USD and another in MXN.

2. Outdated: It looks like this Kickstarter data set was pulled early in 2017. I would want an updated data set if I was going to make decisions based on this today, in 2021. 

- What are some other possible tables and/or graphs that we could create?

1. Given that the scope of the data is international, it might help to understand trends specific to the country in which Louise is looking to launch her play. You could set up a pivot table to see that most Kickstarter campaigns for plays took place in the US and GB. You could then do other research specific to a certain country.

![Country Pivot](/Resources/Theater_Outcomes_by_Country_Pivot.png)

2. You might also want to understand the big picture, such as what percent of Kickstarters relate to theater, and how does the success rate of the theater category compare to that of other parent categories. You could set up a pivot table and stacked column chart to see this. The counts indicate that theater Kickstarters made up 34% of all completed campaigns, and that 61% of those campaigns were successful. The only category with a better success rate is music campaigns.

![Outcome by Parent Chart](/Resources/Kickstarter_Outcome_by_Parent_Category.png)
