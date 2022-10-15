# Amazon_Vine_Analysis

## Overview

There is some concern of bias towards some of the Amazon reviews by members of the paid Amazon Vine program. To analyze this data, the ETL(Extract Transform Load) process will be performed on a set of data. After the data is processed through the ETL method, the data will be split between Vine members and non-members, it will be analyzed by finding the total number of votes, the number of five-star votes, and the percentage of five-star votes of each; this will show some idea of the bias. 

## Results:
### Customer Infomation
![customers_df](/Images/customers_df.png)

### Product Infomation &emsp;&emsp;&emsp;&emsp; Review Information
![products_df](/Images/products_df.png)
![review_id_df](/Images/review_id_df.png)

### Vine Information
![vine_df](/Images/vine_df.png)

During the ETL process, four DataFrames were created. Although the information is good to have, the primary focus of these is the Vine Information DataFrame. This DataFrame has all the information to determine if there us bias of the Vine members.

### Non-Member Reviews Count &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp; Vine Member Reviews Count
![Count-Not_Vine_Program](/Images/Count-Not_Vine_Program.png)
![Count-Vine_Program](/Images/Count-Vine_Program.png)

Using the Vine Information DataFrame, the total number of reviews, total number of five-star reviews, and the percentage of five-star reviews were determined for Vine members and non-members. This information was taken and placed into the DataFrames above.

The key comparisons here are:
  * Number of total reviews: Non-members have a total count of 40,471 reviews; Vine members have a total count of 94 reviews
  * Number of five-star reviews: Non-members have a total count of 15,663 five-star reviews; Vine members have a total count of 48 five-star reviews
  * Percent of votes that are five-stars: Non-members have a percentage of 38.7% five-star reviews; Vine members have a percentage of 51.1% five-star reviews

## Summary
The information suggests that there is some bias when conducting the reviews. As seen in the last DataFrames, non-members have a percentage of 38.7% five-star reviews while Vine members have a percentage of 51.1%, which is about a difference of 12%. There are some issues regarding this data, such as the fact there is only a count of 94 members. Another idea to better understand this data is to see the percentage of five-star reviews is done by customer id, splitting them between members and non-members as well. This will allow analysis if it’s a large part of the Vine membership that is bias are a few particular members with multiple reviews. The same can be done with non-members to confirm the reviews are not largely contributed from a smaller group of the whole.   
