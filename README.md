# Amazon Vine Analysis


## Overview:


In this analysis, ratings from paid Vine reviews were compared with ratings from free non-Vine reviews from the AWS dataset of Amazon ratings for US Musical Instruments.  Using the AWS console and Relational Database Service (RDS), a new PostgresSQL database was created to hold the Amazon review data and connect with the PgAdmin interface.  A Google collab python notebook was used for the Extract, Transform, Load (ETL) process for the review of the data from the following url, 
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Musical_Instruments_v1_00.tsv.gz. A second google collab python notebook was used to filter, clean and analyze the data in the SQL tables created from the previous collab notebook using the pySpark library. 

## Results:


* There was a total of 60 paid Vine reviews and a total of 14,477 non-Vine reviews 


* There were 34 Vine reviews with a 5 star rating and 8,212 non-Vine reviews with a 5 star rating


* 56.67% of Vine reviews had a rating of 5 stars and 56.72% of non-Vine reviews had a rating of 5 stars



## Summary:


In this analysis, the percent of 5 star reviews for paid Vine and free non-Vine reviews were similar at 56.67% and 56.72% respectively.  This similarity suggests there is little evidence for a positivity bias for 5 star reviews between paid Vine and non-Vine reviews.  A caveat is the number of reviews for each review type. The sample size for Vine reviews was only 60, compared with a sample size of 14,477 for non-Vine reviews.  An additional analysis finding the percent of positive reviews with a rating greater than 3 for both reviewer types, Vine and non-Vine, could provide more support for the presence or lack of a positivity bias. In addition, calculating summary statistics including the average and median rating score for Vine and non-Vine reviews would provide more information on possible biases between review types.  Finally a t.test comparing the Vine review results with all of the non-Vine review results could provide details on how significant the differences between review types are.   
