# eCommerce Back End

## Description
A back end system and API to enable online retail managers to manage, organize, categorize and tag their products. The system is a Node.js server running Express, and takes advantage of the Sequelize ORM package for interfacing with a MySQL database.

## Features

The system provides the following API routes:
* `[GET]` `/api/categories` - retrieve a list of current category names and IDs
* `[GET]` `/api/categories/:id` - retrieve the name and ID of a single category
* `[POST]` `/api/categories` - create a new category<br>
  JSON request body, e.g.,
  ```
  {
    "category_name": "Toys" 
  }
  ```
* `[PUT]` `/api/categories/:id` - update the specified category's name<br>
  JSON request body, e.g.,
  ```
  {
    "category_name": "Sports Toys"
  }
  ```
* `[DELETE]` `/api/categories/:id` - delete the specified category
* `[GET]` `/api/tags` - retrieve a list of current tag names and IDs
* `[GET]` `/api/tags/:id` - retrieve the name and ID of a single tag
* `[POST]` `/api/tags` - create a new tag<br>
  JSON request body, e.g.,
  ```
  {
    "tag_name": "science" 
  }
  ```
* `[PUT]` `/api/tags/:id` - update the specified tag's name<br>
  JSON request body, e.g.,
  ```
  {
    "tag_name": "chemistry"
  }
  ```
* `[DELETE]` `/api/tags/:id` - delete the specified tag
* `[GET]` `/api/products` - retrieve a list of current products
* `[GET]` `/api/products/:id` - retrieve the data for a single product
* `[POST]` `/api/products` - create a new tag<br>
  JSON request body, e.g.,
  ```
  {
    "product_name": "superball",
    "price": 0.59,
    "stock": 500,
    "category_id: 3,
    "tagIds": [3, 4]
  }
  ```
* `[PUT]` `/api/products/:id` - update the specified product's details<br>
  JSON request body, e.g.,
  ```
  {
    "product_name": "Superball Hat",
    "price": 20.59,
    "stock": 500,
    "category_id": 4,
    "tagIds": [3, 4, 5, 6]
  }
  ```
* `[DELETE]` `/api/products/:id` - delete the specified product

## Installation
1) Make sure you're running a recent version of [Node.js](https://nodejs.org/en/) (built on v14.16.1)
2) Clone the repository at https://github.com/costanza13/e-commerce-back-end
3) Run `npm install` in the project root directory
4) Make sure you have MySQL installed
5) Copy/rename the sample `.env.sample` file to `.env` and replace the values with your MySQL connection details
6) Run the following to create the `ecommerce_db` database
  > `mysql -u <db_user> -p db/schem.sql`
7) For testing purposes, seed the database using the following command:
  > `npm run seed`

## Running the eCommerce Back End
- Run `npm start` from the project's root directory
  A walkthrough video demostrating startup and functionality can be seen below:

<a href="https://drive.google.com/file/d/1kl9i0vlAMQPjGOQlBmjQs2kwxdRfArb8/view?usp=sharing"><img src="./assets/images/eCommerce-Backend-demo.gif"></a>

## Technologies Used
* Node.js
* Express
* Sequelize ORM
* MySQL

## Credits

This app uses the following very helpful NPM packages:
- [Sequelize.js](https://www.npmjs.com/package/sequelize)
- [Node MySQL 2](https://www.npmjs.com/package/mysql2)
- [Express](https://www.npmjs.com/package/express)
- [dotenv](https://www.npmjs.com/package/dotenv)

## Links
* GitHub: [eCommerce Back End](https://github.com/costanza13/e-commerce-back-end)
* [Demo video](https://drive.google.com/file/d/1kl9i0vlAMQPjGOQlBmjQs2kwxdRfArb8/view?usp=sharing)
