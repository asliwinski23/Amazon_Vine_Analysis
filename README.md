# Amazon_Vine_Analysis

## Project Overview
The POV for this project is that I am a data analyst hired at a consulting firm focused on helping their clients optimize marketing startegy. One particular client in the Entertainment industry, specifically within toys, is looking to release a large catalog of products on Amazon's marketplace. This client wants to understand how reviews of their products stack up to competitors reviews. Additionally, our client is considering enrolling in a program that gives gifts to select reviewers, the Amazon Vine Program, but want to understand if it is actually worth the cost. 

## Resources
Data: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Toys_v1_00.tsv.gz

Toolbox: Spark, Python, SQL, Google Colab, Jupyter Notebooks, pgAdmin, Amazon S3

## Results
In terms of the analysis of the Amazon Vine Program, we filtered the reviews to retrieve all the rows where 'total votes' count was equal or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors later on. Of this subset of the data, 1,266 (2%) reviews came from the program, whereas 62,028 (98%) reviews did not.

This analysis was then taken a step further and I only consdiered 5 star reviews in our subset. Of the 5 star reviews, 47% came from the vine program while 53% did not. Considering the fact that the ratio of paid to unpaid reviews is 2:98, the balance in paid vs unpaid 5 stars reviews in rather significant and indicates that many of the paid reviews were positive.

## Summary
We certainly would recommend enrolling in the Amazon Vine Program to our client based on the data we have. 

Because we did take a subset of our data there is certainly bias. I ran all available review data in a separate notebook. This analysis did not only account for reviews with 'total votes' count equal or greater than 20. When I included all reviews, there was still an overwhelming majority of unpaid reviews compared to paid. However, in this analysis, 85% of the 5 star reviews came from paid reviews. This number is significantly higher than the 47% we saw in the first analysis. 

As a next step, our team would look into specific competitor's consumer sentiment data.
