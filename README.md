# Chocolate Bar Ratings – What makes a good chocolate?


Hello, everyone! In this repository, I'm going to present conclusions about analysis of a dataset called Chocolate Bar Ratings.

# INTRODUCTION. ABOUT VARIABLES.
We all know that chocolate is one of the favorite food in the whole world, possibly even yours, so you must've know that every chocolate has its own flavor and texture. People like Brady Brelinski, Founding Member of the Manhattan Chocolate Society (Flavors of Cacao) have compiled ratings of some of the variables of cocoa or chocolate.
The database I found on Kaggle website (https://www.kaggle.com/rtatman/chocolate-bar-ratings) (there is an updated version on the original page - http://flavorsofcacao.com/chocolate_database.html), focuses only on plain dark chocolate.
The variables that are being chosen here for analysis are:
1) Company (maker-if known) - name of the company manufacturing the bar
2) Specific bean origin or bar name - the specific geo-region of origin for the bar
3) REF - a value linked to when the review was entered in the database. The higher the value - the more recent it is.
4) Review Data - date of publication of the review
5) Cocoa Percent - cocoa percentage (darkness of the chocolate) of the chocolate bar being reviewed - I changed it into relative numbers (60% = 0.60)
6) Company Location - manufacturer base country
7) Rating - expert rating for the bar
8) Bean Type - the variety of bean used, if provided
9) Broad Bean Origin - the broad geo-region of origin for the bean.

Since the names of the variables are a bit long, I have narrowed them down with code. This way, the new variables names are still recognizable, but easier to work with. Every variable is pretty much straightforward, except maybe the Rating variable. 

When talking about rating, the system is following, and it concerns the flavor:
5 = Elite, 4 = Premium, 3 = Satisfactory, 2 = Disappointing, 1 = Unpleasant/unpalatable

# TABLE OF CONTENTS
1) Summary of variables & graphics
  1a) FIVENUM
  1b) Graphics - histograms, boxplot, scatterplots...
2) Correlation analysis?
  2a) Correlation between numeric variables
  2b) Correlation between non-numeric variables (checking the connection)
3) Regression analysis?

You can find the code itself in a different PDF, here I'll just state the conclusion I got from the analysis.

# CONCLUSION
Most of the variables here are not numeric, or can't be functioned with summary and histogram, to see their outliers. In categorical variables, you don't have outliers per-se, so you are very limited in the descriptive statistics with what you can do with it. On the other hand, numerical variables (interval, ratio) can be functioned with summaries, you can calculate their mean, median, see their outliers, but also perform a lot more tests than on categorical variables.
In this dataset, the only numerical variables worth noticing right now are Cocoa percentage and Rating. Here's what the summaries are telling us:

![image](https://user-images.githubusercontent.com/71931115/125800767-5938a2cc-2774-4b87-affc-4a5f2d297520.png)


Here you can see the histogram and boxplot of the variable Cocoa percentage. The red line is representing mean value. Although the difference between the median and mean is small, we can see on the graph that difference isn't that small. Again, since the median is slightly lower than the mean, we can talk about positive skewness, which isn't visible here but it is on boxplot. Also, boxplot shows outliers on both side.

![image](https://user-images.githubusercontent.com/71931115/125800814-b1ffc11f-d9c7-4246-980c-f577cf955c71.png)

![image](https://user-images.githubusercontent.com/71931115/125800834-b3e2968f-455a-4aca-8b44-af79756f8d22.png)

  
Rating variable-wise, the average rating of chocolates in the dataset is 3,228, with standard deviation of 0.46 (half a rating). Also, on the boxplot and histogram, you can visibly see outliers. 

![image](https://user-images.githubusercontent.com/71931115/125800935-3951dccd-d206-4831-b3e7-4df66fbd484b.png)

![image](https://user-images.githubusercontent.com/71931115/125800972-8bd65c5c-f572-4d73-8be6-9ae3cc454810.png)


On the graph below, you can see the relationship between two variables – cocoa percentage and rating. As you can see, it is not linear, which is the key prerequisites for linear regression model.

![image](https://user-images.githubusercontent.com/71931115/125800865-ef5464ba-c0dd-41a9-8863-e1e218be3264.png)

 
Since the distributions aren’t normal and without outliers, but also they don’t have linear relationship between them, I can’t calculate correlation, nor do regression analysis properly. The prerequisites of correlation and regression is that the variables need to have a normal (bell-like) distribution, without any significant outliers and a linear relationship between two posed variables. None of those prerequisites are being found here as they are. Because of that, I’m going to pass on those analyses.
Even if I do perform regression analysis, its R2 coefficient is very low (R2 shows the percentage of variability “catched” by the model).

