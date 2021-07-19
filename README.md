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

There were outliers in the Rating and Cocoa percentage, so I've deleted them and continued working with normal distribution data. Sadly, the correlation coefficient was very low, and we can conclude there was no relationship between variables Rating and Cocoa percentage. Since the correlation was low, the regression analysis was also not successful.

In the PDF called Chocolate Bar Ratings, you can see the full code and my way of thinking, and in the Excel file you can view 3D Maps of the categorical variables - company location, and beans (broad and specific) origin.

