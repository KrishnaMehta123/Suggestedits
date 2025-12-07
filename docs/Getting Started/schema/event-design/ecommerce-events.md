---
title: E-commerce Events
excerpt: 'Event Design Helper: E-commerce platform'
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Sample Custom Events

Below are the essential events that should be tracked on your e-commerce platform to monitor your user interactions and behaviors:

| Event             | Event Property           | Description                                                                                     | Data Type |
| :---------------- | :----------------------- | :---------------------------------------------------------------------------------------------- | :-------- |
| Login             |                          | Recorded when a user logs in.                                                                   |           |
|                   | Method Used              | Mode of login (e.g., Email, Phone, Social Media).                                               | String    |
|                   | Status                   | Indicates login status (success or failure).                                                    | String    |
| Sign Up           |                          | Captured when a user signs up.                                                                  |           |
|                   | Register Option          | Indicates method of registration.                                                               | String    |
|                   | Status                   | Indicates sign-up status (success or failure).                                                  | String    |
| Searched          |                          | Captured when a user searches for a product.                                                    |           |
|                   | Keyword                  | Search keyword entered by the user.                                                             | String    |
|                   | Number of Search Results | Number of search results returned.                                                              | Integer   |
|                   | Number of Out of Stocks  | Number of out-of-stock items.                                                                   | Integer   |
| Category Viewed   |                          | Captured when a user views a product category.                                                  |           |
|                   | Category Name            | Name of the product category the user viewed (e.g., Electronics).                               | String    |
| Product Viewed    |                          | Captured when a user views a specific product.                                                  |           |
|                   | Product Name             | Name of the product viewed (e.g., Headphones).                                                  | String    |
|                   | Product ID               | Identifier for the product (e.g., SKU).                                                         | String    |
|                   | Category                 | Name of the product category (e.g., Electronics).                                               | String    |
|                   | Selling Price            | Price of the viewed product.                                                                    | Integer   |
|                   | Stock Availability       | Indicates if the product is in stock. The _Buy Now_ button appears when the stock is available. | String    |
| Added to Cart     |                          | Captured when a user adds a product to the cart.                                                |           |
|                   | Product Name             | Name of the product added to the cart.                                                          | String    |
|                   | Product ID               | Unique identifier for the added product (e.g., SKU).                                            | String    |
|                   | Category                 | Category of the added product (e.g., Electronics).                                              | String    |
|                   | Product Price            | Price of the added product.                                                                     | Integer   |
|                   | Quantity                 | Quantity of the added product.                                                                  | Integer   |
| Checkout Complete |                          | Captures the checkout details when a user completes the checkout process.                       |           |
|                   | Product Name - X         | Name of product X in the completed checkout.                                                    | String    |
|                   | Price - X                | Price of product X.                                                                             | Integer   |
|                   | Quantity - X             | Quantity of product X.                                                                          | Integer   |
|                   | Product Name - Y         | Name of product Y in the completed checkout.                                                    | String    |
|                   | Price - Y                | Price of product Y.                                                                             | Integer   |
|                   | Quantity - Y             | Quantity of product Y.                                                                          | Integer   |
|                   | Total Price              | Total price of all items at checkout.                                                           | Integer   |
|                   | Total Quantity           | Total quantity of items in the checkout.                                                        | Integer   |
| Support Initiated |                          | Records when a user initiates a support request.                                                |           |
|                   | Support Type             | Type of support initiated.                                                                      | String    |
|                   | Resolved                 | Indicates if the issue is resolved.                                                             | Boolean   |
|                   | Supported Member         | Details of the supported member.                                                                | String    |
| Check Orders      |                          | Recorded when a user checks their order details.                                                |           |
|                   | Product ID               | Identifier for the ordered product.                                                             | String    |
|                   | Product Name             | Name of the ordered product.                                                                    | String    |
|                   | Delivery Date            | Expected delivery date of the order.                                                            | Date      |

Additionally, refer to the [Sample Ecommerce Events Sheet](https://docs.google.com/spreadsheets/d/1nMdjjjyOUvgwJEGQp7AsKbrIATToyySEue9cA027tA8/edit?usp=sharing).