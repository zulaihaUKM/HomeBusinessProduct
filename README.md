# Shopee Home Business Product
Home business is a business whose primary office is within their home regardless of the size of the office as long as it is located at home. Various home businesses can be done such as bakery business, crafty ideas, online retail, soap making, skin care &amp; beauty, and many more. This project aims to collect and share information on the findings of several products sold as home business through the Shopee application platform in Malaysia. The obtained data is then stored in the form of sql and csv file format so it can be used by individuals in need for their own research needs.
## About Project
A total of 14,328 home-business based products on Shopee were compiled into a sql and csv file to facilitate knowledge sharing for any individual who needed the data for research purposes. In the sql file, this data has been divided into 7 data tables. The tables are namely stores, products, product_attributes, product_models, product_variations, product_reviews and product_ratings. To understand the function of each table and all the attributes in it, the description is as follows:
> store table : information about the store of product(s)
- id : unique number for each store
- username : user name used by the store (ie: @abc_cookies)
- logo : link of the image that used to represent the store
- follower count : number of store follower on Shopee
- shopee verified : store verification status on Shopee
- product count : number of products posted on Shopee
- name : name used by the store (ie: ABC Cookies)
- place : basic address of the store located
- rating bad : number of bad rating from users
- rating good : number of good rating from users
- rating normal : number of neutral rating from users
- rating star : overall rating star given for the store (ie: 4.3/5 star)
- response rate : the percentage of response time between seller and customers chat
- response time : the number of times the seller had responses to customer chat
- shop location : state of the store located
- joined date : date of store registered on Shopee
- created at : date of store account created 
- updated at : date of store information updated
> product table : product information sold in shopee
- id : unique number for each product
- price max before dicount :
- price before discount :
- price min before discount :
- price min :
- price max :
- price :
- stock :
- discount :
- sold :
- name :
- description :
- brand :
- rating star :
- rating count :
- images :
- image :
- videos : 
- category :
- shop location :
- created at :
- updated at :
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
