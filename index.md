# Boston Airbnb

Watching and exploring the information inside the 3 datasets of Boston Airbnb service who have information between 2016-09 to 2017-09 there are many question one could ask, looking deeply I define 3 questions using 2 of the 3 datasets. The first dataset named "calendar"  have the records of booking , the second named "listings" have all information about all airbnb that somedody could rent in the city of Boston and the last one named "review" contain the review of people who rented some place in airbnb.

## Question 1
 Availability per month and mean price per month have the same behavior in the boston Airbnb rents?

### Solving the problem

Looking at the data I want know if the month determine if the prices of the average of renteded house increase in speficic months(high season) or if the availibily depend of time in year and make conclusions about this two cases. The next two plots help to solve this question

![image](https://user-images.githubusercontent.com/88516507/128954566-1794dac3-3ad8-4eca-8c7e-39144a90d709.png) ![image](https://user-images.githubusercontent.com/88516507/128954617-8aa91074-d4f7-484e-9dd9-376fc8cecdb7.png)

We can see at the begin of time window the average price tends to decrease and number of the available propertys tends to increase. Between march to august the price present small variaton, same as the number of the available properties. The conclussion is at the first semester the plots show contrary behaviors and in the second semester they are similar.


## Question 2
Are necessesary in the "listings dataset" 7 columns of review's ?

### Solving the problem

Thinking about how I could optimize the compilation of any model data , one way is drop those columns that explain the same things. So looking all columns of this database I found that 7 columns start with the word review, so I wondered if those columns presents high correlation. The next plot show the correlation between columns:

![image](https://user-images.githubusercontent.com/88516507/128956608-bee76745-8399-4e53-b637-d2f93c64d330.png)

In first place we can see positive correlation in all columns and taking as example the columns "review scores rating" we can see high correlations (>0.7) in 3 of 6 columns son if we want to use "review scores rating" in a model data, we should drop the columns with high correlation to avoid an overfiting in the model.


## Question 3
If somebody wants to put in rent any of their properties in Airbnb, what variables are the most important to make sure that the property will be rented more than 50% of time in a year ?

### Solving the problem
