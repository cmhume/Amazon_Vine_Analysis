# Amazon Vine Analysis


## Overview:


In this analysis, ratings from paid Vine reviews were compared with ratings from free non-Vine reviews from the AWS dataset of Amazon ratings for US Musical Instruments.  Using the AWS console and Relational Database Service (RDS), a new PostgresSQL database was created to hold the Amazon review data and connect with the PgAdmin interface.  A Google collab python notebook was used for the Extract, Transform, Load (ETL) process for the dataset linked below. A second google collab python notebook and the pySpark library was used to filter, clean and analyze the same Vine and non-Vine review dataframes that were also made in the first collab notebook. 


Dataset: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Musical_Instruments_v1_00.tsv.gz


ETL google collab notebook: https://github.com/cmhume/Amazon_Vine_Analysis/blob/530aa7d4cfcfd192a8d061137560969207f44a51/Amazon_Reviews_ETL.ipynb


Analysis google collab notebook: https://github.com/cmhume/Amazon_Vine_Analysis/blob/5f2828a56e9191e8c4b8170262055698076e5ce3/Vine_Review_Analysis.ipynb


## Results:


* There was a total of 60 paid Vine reviews and a total of 14,477 non-Vine reviews 


* There were 34 Vine reviews with a 5 star rating and 8,212 non-Vine reviews with a 5 star rating


* 56.67% of Vine reviews had a rating of 5 stars and 56.72% of non-Vine reviews had a rating of 5 stars


### Creating unpopulated tables in PgAdmin

![pgadmin_create_tables](https://user-images.githubusercontent.com/78699521/124401243-26192f80-dcdd-11eb-8f9f-3543e836fc99.png)


### Loading data into PgAdmin with google collab notebook


ETL google collab notebook: https://github.com/cmhume/Amazon_Vine_Analysis/blob/530aa7d4cfcfd192a8d061137560969207f44a51/Amazon_Reviews_ETL.ipynb


### Populated tables in PgAdmin after ETL process in google collab notebook


![load_vine_table](https://user-images.githubusercontent.com/78699521/124401253-3204f180-dcdd-11eb-8a7f-224225c175a6.png)


![load_customers_table](https://user-images.githubusercontent.com/78699521/124401262-3b8e5980-dcdd-11eb-854c-dc0115a55130.png)


![load_products_table](https://user-images.githubusercontent.com/78699521/124401268-40530d80-dcdd-11eb-8455-79707403aa77.png)


![load_review_id_table](https://user-images.githubusercontent.com/78699521/124401272-46e18500-dcdd-11eb-9e70-ccd7b60a6c50.png)


### Analysis of data in google collab notebook


Analysis google collab notebook: https://github.com/cmhume/Amazon_Vine_Analysis/blob/5f2828a56e9191e8c4b8170262055698076e5ce3/Vine_Review_Analysis.ipynb


![filter_num_votes](https://user-images.githubusercontent.com/78699521/124401175-ae4b0500-dcdc-11eb-8b87-948eb7654539.png)



![review_analysis](https://user-images.githubusercontent.com/78699521/124401184-b7d46d00-dcdc-11eb-8b49-de29b5f3b423.png)





## Summary:


In this analysis, the percent of 5 star reviews for paid Vine and free non-Vine reviews were similar at 56.67% and 56.72% respectively.  This similarity suggests there is little evidence for a positivity bias for 5 star reviews between paid Vine and non-Vine reviews.  A caveat is the number of reviews for each review type. The sample size for Vine reviews was only 60, compared with a sample size of 14,477 for non-Vine reviews.  An additional analysis finding the percent of positive reviews with a rating greater than 3 for both reviewer types, Vine and non-Vine, could provide more support for the presence or lack of a positivity bias. In addition, calculating summary statistics including the average and median rating score for Vine and non-Vine reviews would provide more information on possible biases between review types.  Finally a t.test comparing the Vine review results with all of the non-Vine review results could provide details on how significant the differences are between paid and free review types.   
