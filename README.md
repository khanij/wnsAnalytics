# wnsAnalytics
WNS Analytics Wizards competition 2019

## Problem Statement: https://datahack.analyticsvidhya.com/contest/wns-analytics-wizard-2019/

## Approach :

We see the given problem as binomial logistic regression. We need to predict whether the user will click the ad impression or not. Based on **Viewlog and item log**, we build the **user profile** with the following attributes.

- user_id                      
- total_search_count           : Number of searches the user has done on Zbay     
- no_of_sessions               : Number of times user has logged onto Zbay.
- no_of_unique_items           : Number of Unique items that the user has searched.
- frequent_item                : Frequent item that the user has searched for 
- frequent_item_search_count   : Number of times the user has searched his/her recent item
- recent_device                : recent device user has user for last login
- recent_item_searched         : recent item that the user has searched for
- recent_search_time           : recent search time 
- freq_item_price              : price of frequent item that the user has searched for 
- freq_prod_type               : Product type of the frequent ite
- freq_item_length             : Length derived as category1+category2+category3 
- freq_no_of_items             : Number of items in the product type of the product 
- freq_prod_length             : Product type length of the frequent item 
- freq_max_price               : Max Price for product type of the frequent item 
- freq_min_price               : Min Price for product type of the frequent item
- rec_item_price               : Recent item price 
- rec_prod_type                : Product type of the recent item 
- rec_item_length              : item length of the recent item 
- rec_no_of_items              : number of items in product type of the recent item 
- rec_prod_length              : Lenght of product type of the recent item 
- rec_max_price                : Max Price for product type of the recent item  
- rec_min_price                : Min Price for product type of the recent item  

We enrich the **Impression data** with the above user profile(based on user id) and build a logistic regression using the resultant data set.


We also derive the following attributes using impression data.

- ad_rn : Corresponding rank of the impression ( like 1st ad, 2nd ad, ... nth ad)
- Time to Ad: Time difference between the impression and last search time of the user
