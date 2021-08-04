"An analysis of Kickstart campaign data using Excel functions and formatting" a data project by Stefan Johnson.  

--Background on Project--

Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. For this project, I organized and analyzed a database of 4,000 past projects to look for hidden trends.

Please read on for a detailed overview of the steps I took to complete this project.

--Initial formatting--

I used condtional formatting to fill each cell in the "state" column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.
I created a new column O called "Percent Funded" that uses a formula to display how much money a campaign made to reach its initial goal.

I used conditional formatting to fill each cell in the "Percent Funded" column using a three-color scale. 0 being a dark shade of red, transitioning to green at 100, and blue at 200.

I created a new column P called "Average Donation" that uses a formula to show how much each backer for the project paid on average.

Created two new columns, one called "Category" at Q and another called "Sub-Category" at R, which uses formulas to split the "Category and Sub-Category" column into two parts.

--Organizing data for analysis--

Created a new sheet with a pivot table to analyze how many campaigns were successful, failed, canceled, or are currently live per category.

Created a stacked column pivot chart that can be filtered by country.

Created a new sheet with a pivot table to analyze initial worksheet and count how many campaigns were successful, failed, or canceled, or are currently live per sub-category.

Created a stacked column pivot chart that can be filtered by country and category.

In "Launched" column, converted Unix timestamps to normal date via a formula and then stored values in a new column named "Date Created Conversion".

In "Deadline" column, used same formula as above to convert Unix timestamps and store values in a new column named "Date Ended Conversion"

Created a new sheet with a pivot table with a column of `state`, rows of "Date Created Conversion", values based on the count of "state", and filters based on "parent category" and "years".

Created a pivot chart line graph to visualizes this new table.

Created a new sheet with 8 columns:

  * Goal
  * Number Succesful
  * Number Failed
  * Number Canceled
  * Total Projects
  * Percentage Successful
  * Percentage Failed
  * Percentage Canceled

In the `Goal` column, created 12 rows with the following headers:

  * Less than 1000
  * 1000 to 4999
  * 5000 to 9999
  * 10000 to 14999
  * 15000 to 19999
  * 20000 to 24999
  * 25000 to 29999
  * 30000 to 34999
  * 35000 to 39999
  * 40000 to 44999
  * 45000 to 49999
  * Greater than or equal to 50000

I used the countif formula to count how many successful, failed, and canceled projects were created with goals within the ranges listed above. 

Summed up each of the values in succesful, failed, and canceled columns to populate the total column. Then, used a formula to find the percentage of projects that were successful, failed, or canceled per goal range.

Created a line chart that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.

--Summary Statistics Table--

Evaluated the following for successful campaigns, and then for unsuccessful campaigns:

  * The mean # of backers.

  * The median # of backers.

  * The minimum # of backers.

  * The maximum # of backers.

  * The variance of the # of backers.

  * The standard deviation of the # of backers.

I also provided some analysis on my findings within the excel worksheet.  
