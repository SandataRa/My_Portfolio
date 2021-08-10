# [Project 4: Amazon bestsellers from 2009 to 2019](https://www.kaggle.com/sootersaalu/amazon-top-50-bestselling-books-2009-2019/tasks?taskId=2741)

This dataset contains the bestsellers books from 2009 to 2019 on Amazon for a total of 550 rows and 7 columns. This project is an Exploratory Data Analysis aiming
to identify the common characteristics of best sellings books on Amazon's marketplace. 

This project was realized during my **#20daysDataScience2021** challenge.

## Exploratory Data Analysis 
The first step is to observe the different distributions to have a general overview of the dataset. The series of graphs below are our support of analysis.
The first histogram is displaying the distribution of observations by Price. The best selling books have a price ranging mainly between **5$ to 20$**. 
After that threshold, the number of observations drops drastically. It is interesting to note that a low price is an essential attribute among bestsellers.  

![Price simple hist](/images/p4_price_simple_hist.png) 
  
The number of reviews can give us an approximate value of the number of sales for each book. **The number of reviews** is following the same distribution as 
the price with a **threshold at 20K reviews**. It’s interesting to note that some books managed to break that glass ceiling and earn more than **60K reviews**. 
From the histogram (see below) we can see that some books are doing even better than the majority of bestsellers.  

![Reviews simple hist](/images/p4_reviews_simple_hist.png)  
  
During 10 years, we can observe a **bigger interest for non-fiction books over fiction**. With more than **300 bestsellers**, non-fiction books are more popular
on Amazon. Let’s observe how this trend evolves during the decade.  

![Year & Genre hist](/images/p4_year_genre_bivar_hist.png)  

Over the decade, the upper histogram is showing that the majority of bestsellers are **non-fiction** books.
The only exception is **2014 where fiction dominated the segment**. This observation is confirmed with the KDE graph below.

![year & Genre kde](/images/p4_year_genre_kde.png)  

Now that we have identified a second attribute of the best sellers, let’s observe **Price** and **Genre**. The following graph confirms our first observation regarding 
the price’s trend. If we focus on the books above the **20$ threshold**, we observe a majority of non-fiction books.  

![Price & Genre hist](/images/p4_price_genre_bivar_hist.png)  

The following histogram is displaying the distribution of observations across rating levels. Most of our observations concern books with a rating over **4.4** which 
confirms that being a bestseller is linked deep to the book’s rating. The higher the book’s rating on Amazon, the higher is its probability to become a bestseller. 
Confirming our previous comments, *non-fiction books with good ratings have a higher probability of becoming a bestseller on Amazon*.  

![Rating & Genre hist](/images/p4_rating_genre_bivar_hist.png)

Amazon gained popularity across the year, let’s see if this assumption is confirmed with the data. Using the scatterplot below, we can see that the number of reviews 
stayed **constant for 10 years with some peaks between 2013 until 2016**. Even though non-fiction books are more popular among bestsellers, we can see that fiction books 
have more reviews in comparison to its opposite.  
  
But since **2018**, it seems that non-fictions books are slowly earning more reviews with **2 bestsellers** cumulating more than 60 000 reviews.  
  
![Year & Reviews scatterplot](/images/p4_year_review_scatter.png)  
  
  
Let’s compare these two genres a little bit more with the following scatterplots. This visualization confirms that most bestsellers have less than **40K reviews** and 
that their ratings are usually above the **4.4** mark. This trend is the same during the entire decade until **2018**. It’s important to observe that fiction contains more 
outliers in comparison to the non-fiction side which is much more homogeneous. Another important observation is the year **2010** where more of the books have few reviews 
(*below 10K*) in both genres.  

![Reviews dual scatterplot](/images/p4_reviews_rating_scatter_duo.png)





  
  
  

