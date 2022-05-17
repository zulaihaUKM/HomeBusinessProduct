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
- shop location : state of shop location
- created at : date of product post created
- updated at : date of product information updated
> product attributes table : information of attributes in each product
- id : unique number for each product attribute
- product id : unique number of product
- name : name of product attribute (ie: pack size/ shell life/ weight)
- value : value of each attribute (ie: 1 pack/ 12 months/ 150g)
- created at : date of product attribute created
- updated at : date of changes made on product attribute
> product variations table : list of variations available for each product
- id : unique number for each product variation
- product id : unique number of product
- name : name of product variation (ie: size/ flavour)
- options : list of product variation (ie: small,medium,big / original,sweet,spicy)
- images: link of product image
- created_at: date of product variation created
- updated_at: date of changes made on the product
> product models table : detailed information about each product variation
- id : unique number for each product model
- product id : unique number of product
- name : name of a variation in a product (ie: 3x spicy)
- price : price of the product
- stock : number of stock available
- price before discount :  price of the product before discount is applied
- extinfo : extra information / description about the product model (ie: type: 3x spicy, weight: 150g)
- created at : date of product model created
- updated at :  date of changes made on product model
> product ratings table : information of product rating made by customer
- id: unique number of each product rating
- product id: unique number of product
- rating total: total number of rating given to product
- rating with context: number of rating that has feedback written by customer
- rating with image: total number of images attached in product rating by customers
- rating with media: total number of images and videos attached in product rating by customers
- ratings: total number for each rate (ie: {"all": 3, "1": 0, "2": 0, "3": 0, "4": 0, "5": 3} <br> means that there are 3 ratings in total, no one rating for 1-4 stars, and 3 person have rate for 5 stars)
- created at: date of first rating made
- updated at: date of changes made on product rating
> product reviews table : information of product review made by customers after giving product rating
- id: unique number for each review made
- product id: unique number for each product
- product rating id: unique number of product rating
- username: username of customer account on Shopee
- comment: feedback/ comment made by customers regarding purchased product
- profile picture: link of image of customer profile picture
- images: link of image attached within the product review
- rating star: star rating given by customer
- rating: differentiate between bad or good rating (0 for bad and normal rating, and 1 for good rating)
- region: country code of product region
- videos: link of video attached in product review
- reply: product review reply from seller
- created at: date of product review created
- updated at: date of changes made on product review
## Data Relation
The figure of data relationship of collected data is shown as in the file attached, named 'Shopee Product Table Relationship.png'. Below are the explanations regarding the relationship between each table:
> Relation Between ***stores*** and ***products*** Tables
 - Each registered product on Shopee should be owned by one and only one store. However, a store could registers one or more product on Shopee. Thus, the relationship between ***stores*** and ***products*** table is one-to-many(1:M).
> Relation Between ***products*** and ***product_attributes*** Tables
- Each product must have at least one attribute like its weight, country of origin, expiry date, size, and etc for product description. A product could also have more than one attribute described by seller on Shopee. This makes the relationship between ***products*** and ***product_attributes*** becomes one-to-many(1:M) relation.
> Relation Between ***products*** and ***product_variations*** Tables
- Each product will have at least 1 variation registered on Shopee. However, there are some products that are registered with more than one variation like variety of pack sizes, colour options, flavours, weights and many more. For example, a potato chip product can either be sold with only original flavour or sold with 3 different flavours (original, sweet, barbeque). It can be said that the relationship between ***product*** and ***product_variation*** tables is one-to-many(1:M) relationship.
> Relation Between ***products*** and ***product_models*** Tables
- In Shopee, every product has their own product details which are called as product model. Each product should have at least one or many model registered. For example, a potato chip has 3 different flavour variations so, there are also 3 models for the product (representing each type of variations). The product model for barbeque potato chip flavour could be written as {type:barbeque, pack size: small, weight: 75g}. It can be that the relationship between ***products*** and ***product_models*** tables one-to-many(1:M) relationship.
> Relation Between ***products*** and ***product_ratings*** Tables
- After a product is successfully sold to a customer, a product rating can be made to rate the product quality. One product can have one or many buyer and receives multiple ratings from customers. However, there are also products that do not have any rating because there is no buyer or rating made by customer. Still, the relationship between the ***products*** and ***product_ratings*** tables is seen as one-to-many(1:M) relationship.
> Relation Between ***products*** and ***product_reviews*** Tables
- Same as product rating, customer can make a product review after receiving the purchased item. Product review can contain feedback writing, image, and video attached. One product can have one or more product reviews by customers but there are also products which do not have any product review because of no buyer or there is no customer who make any review yet. The relationship between ***products*** and ***product_reviews*** tables is seen as one-to-many(1:M) relationship.
> Relation Between ***product_ratings*** and ***product_reviews*** Tables
- Each product review should have one and only one product_rating_id. For customer, it is a-must to give a product rating before leaving a review. However, customer can choose either to write a product review or not when giving rate. Therefore, not all product ratings will have review written. The relationship between ***product_ratings*** and ***product_reviews*** tables is one-to-zero-or-one (1:1) relationship.
## To Upload sql File Into Xampp/Laragon
