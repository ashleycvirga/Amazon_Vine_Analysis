# Amazon_Vine_Analysis

Analyzing Amazon reviews written by members of the paid Amazon Vine program with SQL and PySpark.

## Overview

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

This project analyzes Amazon reviews for the category of "Pet Products" to investigate the possibility of bias due to the Amazon Vine program. 

PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then I used PySpark again to determine if there is any bias toward favorable reviews from Vine members in the "Pet Products" dataset. 

Is the percent of reviews that have 5-star ratings greater from Vine members than non-members?

Amazon Reviews Dataset : [Pet Products](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz)

## Results

Total Vine Member Reviews: 170
Total Paid 5-Star Vine Reviews: 65
Paid percentage of Vine 5-Star Reviews: 38.2%

![paid_reviews.png](https://github.com/ashleycvirga/Amazon_Vine_Analysis/blob/3f05bce83dfc4a3ebcdf17d575ac57539a2fce26/Images/paid_reviews.png)

Total Non-Vine Member Reviews: 37840
Total Unpaid 5-Star Reviews: 20612
Unpaid percentage of Vine 5-Star Reviews: 54.5%

![unpaid_reviews.png](https://github.com/ashleycvirga/Amazon_Vine_Analysis/blob/3f05bce83dfc4a3ebcdf17d575ac57539a2fce26/Images/unpaid_reviews.png)


## Summary

So, is there a positivity bias for reviews written by members in the Vine program?

In general, there were far more reviews in the "Pet Products" category written by Non-Vine Members than there were for Vine Program Members.

Slightly over 50% of those non-member reviews were 5 star artings.  While only about 38% of Vine Program member reviews were given 5 star ratings.  

Based on this analysis, I do not see more 5 star reviews given by Vine Program members than non-members and therefore do not see a positivity bias for reviews written by members in the Vine program.


### Recommendations

I would recommend analyzing the average of all ratings given by Vine Members and Non-Members for all product categories to fully determine if there is a difference in average rating for each and every product. More database storage would be necessary to complete that analysis.
