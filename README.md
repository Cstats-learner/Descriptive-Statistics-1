# Descriptive-Statistics 
In the practice, we will filter out bad data, fill in missing values, transform data into a suitable format, and draw appropriate chart.

## Analysis in San Francisco Salary dataset
### Synopsis
Our goal in this analysis is to explore the salaries in San Francisco overtime. What we expected to discover are:
1.	The salary will raise as time goes by. 
2.	The central tendency and variability will increase years over years
3.	The range of salary will increase years over years.

#### Dataset: https://www.kaggle.com/micahshull/san-francisco-salary-data-20122017
The data we have chosen to use is titled “SF Salaries” and was found on kaggle.com. There are over 150,000 dataset containing the employee name, job title, and the compensation for employees in San Francisco city from 2012 to 2017.

### Goal
We want to know tendency of salary in San Francisco during this period. Is there any increase of central tendency or how is the range of maximum and minimum salary.

### Analysis
The library we currently envision using are pandas, numpy, statistics, matplotlib and seaborn.
Individual data points consist of salaries postings containing employee name, position title, base pay, over time pay, other pay, benefits, total pay, total pay benefits, and year. Descriptive statistics will be used to turn the data into different quantity distribution containing the percentage we desire.
Histogram, box plot, and line chart will be used to build the salary scheme. 

#### Task 1: Data wrangling
•	Drop some useless column(note, agency and status):
1.	Drop status marked as PT(part time) row. 
2.	salary.drop([“Note”, “Agency”] ,axis = 1)
•	Impute missing values(Nan)
1.	Detect the variables containing null value: salary.isnull().sum()
2.	Fill the missing values: salary.fillna(value = {given a dictionary mapping the missing value to specific value})
•	Remove negative values 
1.	We found there is one row of data showed negative benefits. The value is abnormal and will affect total value and mean.
2.	Drop rows with negative value

#### Task 2: Measure central tendency
•	Compute the salary statistics(mean, median, mode, minimum, maximum, range, 25% quantile, 50% quantile, 75% quantile ) 
1.	Apply sorted method to compute minimum and maximum and range from minimum and maximum
2.	Import statistics library and apply mean, median and mode methods
3.	import numpy library and apply quantile method

*mean: the average value
*median: the middle value after sorted
*mode: the most frequently occurring value


#### Task 3: Measure variability 
•	Compute the variance and standard deviation of salary
1.	Import statistics library and apply pvariance and pstdev methods

#### Task 4: Suitable charts
Attach the picture, and why we want to use it
•	Histogram of salaries: show the distribution total pay and benefits.
•	Bar chart of people in each year.
•	Boxplot of salaries in annual basis: take the totalPayBenefits as a salary

### Results and Findings 
From this analytics, we can find that the salary in San Francisco is increasing slowly from 2012~2017. By observing mean, median value of each year, the numbers are similar in 2012, 2013, 2016. On the other hand, the value in 2014, 2015, and 2017 are higher. The value of standard deviation can also group into two. It showed that 2014, 2015 have different values lower than others. In the contrast, the range of salary went to a different side to standard deviation and variable. In conclusion, we find the difference of salary from year to year is slight. As this result, we can suggest the government to increase the minimum wage of salary in order to improve welfare of the whole society.   


