# Shopee Home Business Product
Home business is a business whose primary office is within their home regardless of the size of the office as long as it is located at home. Various home businesses can be done such as bakery business, crafty ideas, online retail, soap making, skin care &amp; beauty, and many more. This project aims to collect and share information on the findings of several products sold as home business through the Shopee application platform in Malaysia. The obtained data is then stored in the form of sql and csv file format so it can be used by individuals in need for their own research needs.
## About Project
A total of 14,328 home-business based products on Shopee were compiled into an sql and csv file to facilitate knowledge sharing for any individual who needed the data for research purposes. These products are local products originating from Malaysia and most of them are based on food business. In the sql file, this data has been divided into 7 data tables. The tables are namely stores, products, product_attributes, product_models, product_variations, product_reviews and product_ratings. To understand the function of each table and all the attributes in it, the description is as follows:
> stores table : information about the stores of each product registered on Shopee
- id : unique number for each store
- username : username used by the store (ie: @abc_cookies)
- logo : link of the image that used to represent the store
- follower count : number of store follower on Shopee
- shopee verified : the status of store verification on Shopee (verified/unverified)
- product count : number of products posted on Shopee
- name : name used by the store (ie: ABC Cookies)
- place : basic address of the store location
- rating bad : number of bad rating from users (0-2 over 5 stars)
- rating good : number of good rating from users (4-5 over 5 stars)
- rating normal : number of neutral rating from users (3 over 5 stars)
- rating star : overall rating star given for the store (ie: 4.3/5 star)
- response rate : the percentage of response time between seller and customers chat
- response time : the number of times the seller had responses to customer chat
- shop location : state of the store location
- joined date : date of store registered on Shopee
- created at : date of store account created 
- updated at : date of store information updated
> product table : information of product posted on Shopee
- id : unique number for each product
- price max before dicount : maximum price of product before discount is applied
- price before discount : normal price of product before discount is applied
- price min before discount : minimum price of product before discount is applied
- price min : the minimum/lowest price of product that has been recorded
- price max : the maximum/highest price of product that has been recorded
- price : current price of product
- stock : current total of stock available
- discount : the percentage of current available discount (ie: NULL / 75%)
- sold : total number of products that have been sold
- name : display name of the product
- description : description of product
- brand : brand of product (ie: NULL / ABC Cookies)
- rating star : overall star rating for the product
- rating count : total number of rating given by customer
- images : link of product image
- image : link of product image
- videos : link of product video
- category : category of product sold (ie: processed food/ clothes/ electronic)
- shop location : state of shop located
- created at : date of product post created
- updated at : date of product information updated
> product attributes table : information of attribute in each product
- id : unique number for each product attribute
- product id : unique number of product
- name : name of product attribute
- value : value of each attribute
- created at : date of product attribute created
- updated at : date of changes made on product attribute
> product models table :
- id : unique number for each product attribute
- product id : unique number of product
- name :
- price : 
- stock :
- price before discount : 
- extinfo : extra information / description about product
- created at : 
- updated at : 
> product variations table :
- id : unique number for each product variation
- product id : unique number of product
- name : 
- options : 
> product ratings table :
> product reviews table :
## Data Relation
The figure of data relationship of collected data is shown as in the file attached, named 'Shopee Product Table Relationship.png'. Below are the explanations regarding the relationship between each table:
> Relation of ***stores*** - ***product*** Table
 - Each registered product on Shopee should be owned by one and only one store. However, a store could registers one or more product on Shopee.
 - Thus, the relation of ***stores*** and ***product*** table is 'one:one to one:many'
## To Upload sql File Into Xampp/Laragon
