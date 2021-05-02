# Kickstarting with Excel

## Overview of Project

### Purpose
 
 The prupose of this project was to analyze the Kickstarter dataset to provide Louise with insights on different campaigns. Louise wanted to know how campaigns preformed based on their launch dates and their funding goals. After completing the appropriate analysis in Excel, visualizations also needed to be made to help convey the finidngs of the analysis. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

In order to complete the analysis for outcomes based on launch date, I needed to create a new column in the "Kickstarter" sheet of the workbook that pulled the years of the launch dates. As you can see below, I used the cell that held the launch date as the input for the =YEARS() function. ![=YEARS() Example]("C:\Users\hp\OneDrive\Desktop\Analysis Projects\Module 1\Year function.png") I then created a pivot table (seen below) to display the outcomes based on the launch date of the campaign. ![Outcomes Based on Launch Pivot Table]("C:\Users\hp\OneDrive\Desktop\Analysis Projects\Module 1\outcomes pivot.png") After creating the pivot table, I created a PivotChart to visualize the data in the table. 

### Analysis of Outcomes Based on Goals

For the analysis of outocomes based on goals, I created a new sheet to find the number of successful campaigns, the number of failed campaigns, and the number of canceled campaigns based on their goals. In order to find these numbers I used the =COUNTIFS() function in Excel. As seen below, I inputed the column that held outcomes as my first range and indicated my desired outcome as the criteria. I then inputed the column that held goals as my second range and indicated the lower bound for the goal. I then repeated this and indicated the upper bound for the goal. Then, for my final range I inputed the columns that held subcategories and indicated plays as my criteria. ![=COUNTIFS() Example]("C:\Users\hp\OneDrive\Desktop\Analysis Projects\Module 1\countifs.png")

### Challenges and Difficulties Encountered

The first challenge I encountered was creating the pivot table for the outcomes based on launch date. When I selected "Date Created Conversions" as a row it first only showed up as the years. I figured out that it added years, quarters, and months as variables automatically, so I had to remove the years and quarters from the PivotTable fields to just have the months.

The other challenge I ran into was with using the =COUNTIFS() function. I had no issue when it came to using it for the less than 1,000 goal range and the greater than 50,000 goal range. However, when it came to ranges that had specified upper and lower bounds I struggled for a bit. For example, when looking at the 1,000 to 4,999 range, I tried to use the input =COUNTIFS(Kickstarter!F:F, "successful", Kickstarter!D:D, ">=1000" AND "<=4999",Kickstarter!R:R, "plays"). I eventually realized that I had to look at the two bounds seperately and input it as =COUNTIFS(Kickstarter!F:F, "successful", Kickstarter!D:D, ">=1000", Kickstarter!D:D, "<=4999",Kickstarter!R:R, "plays"). 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The first conclusion you can make about the outcomes based on launch date is that the the mode for number of successful campaigns was in the month of May. The second conclusion that you can make is that the mode for the number of failed campaigns was also in the month of May.  

- What can you conclude about the Outcomes based on Goals?

When looking at the outcomes based on goals, you can conclude that goals of less that 1000 yield the highest success rate followed by goals of 1000 to 4999. You can also conclude that goals of 45000 to 49999 yield the lowest success rates. However, this conclusion is somewhat lacking because there was only one campaign that fell within that goal range.

- What are some limitations of this dataset?

One limitation of this dataset is that there aren't as many campaigns with goal values above 15000. This makes any conclusions about outcomes based on these higher goal values less valid than those with lower goal values because there is more data for the lower ones. Another limitation is that there is not a lot of data for theater campaigns and plays that had been cancelled. 

- What are some other possible tables and/or graphs that we could create?

A table that could be created is a pivot table that looks at the number of backers and the outcomes. This could potentially lend some insight as to how many backers are needed for a successful campaign. Another table that could be created is one that looks at the outcome and country. This could then be turned into a graph to visualize which countries have the most successful campaign outcomes. 
