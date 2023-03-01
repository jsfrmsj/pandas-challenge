# pandas-challenge
Module 4 Challenge

PyCity Schools Analysis

    The schools that spent less than 630 dollars per student dramatically outperformed the schools that spend more that 630 dollars per student. The overall passing percentage rate of schools that spent between 585 dollars to 630 dollars per student was 81%. The overall passing percentage rate of schools that spent between 630 to 645 dollars was just 62%.

    Smaller (less than 1000 students) and medium sized schools (1000 to 2000 student) performed relatively the same with 90% & 91% overall passing respectively. However,the overall passing scores of large sized schools (2000 to 50000 students) dropped dramatically to just 58%.

    Additionally, the top 5 performing schools, based on overall passing percentage, spent less than 638 dollars per student. With an average amount spent between all 5 schools of about 606 dollars per student. Additionally, the average size of the student population between the top 5 schools was approximately 1641 students (medium sized).

    In contrast, the bottom 5 performing schools, based on overall passing percentage, spent an average of 647 dollars per student and had a average student size of 3853 students (large sized).

    Based on this data, it could be suggested that there is a goldent ratio of both school size and spending that could achieve the best results for overall passing rates. However, it is not clear exactly how the schools that spent less per student were able to perform better than schools that spent more per student. Or why smaller sized schools perform better than larger sized schools. Therefore, more analysis in these two aspects is needed to fully understand what can be done to improve school performance across the district.



First I merged the two files with school data and student data into one dataframe with pd merge to the left on school name. This code was given. 

Then I got a basic breakdown of the data at the district level, things like school count, student count, average scores etcetera. Nunique for school count and then the count function for student count. Sum for budget and mean for math/reading scores. Passing math percentage code was given to us, changed the code to get the answer for reading. Then created a new dataframe to display all the district information in one table.

Then I broke down the data by school so that we could see how each school performed. Piggubacking on the code that was given above I was able to do the same basic calculations for each school, math/reading score etcetera. Again, created a dataframe to display the new calculations into a table "per_school_summary". 

Then sorted the values, first as ascending = false to display the top performing schools. Higher percentage overall passing = top performing. Then removed ascending = false to display the bottom performing schools.

First used the loc function to find the math scores by grade level then the grouby function to group the school name and scores . mean to get the average. Repeated for each grade level then creaded a new datafram to display this information. Repeated for reading scores. 

Then created bins and labels for per student spending. Then used pd.cut to categorize the schools based on the spending bins that were created into a dataframe. From there I used the groupby function to show the average scores by each spending bin.

Created bins and labels for school size. Then used pd.cut to categorize the schools based on student population size. From there I used the groupby function to show the average scores by school size.

finally used the groupby function to show the average scores by school type.