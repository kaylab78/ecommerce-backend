# E-commerce Backend
![Github license](https://img.shields.io/badge/license-MIT-blue.svg)

## Description
This is the back end for an e-commerce site that can be managed through the command line interface with API route testing in Insomnia.

Walkthrough Video: [https://drive.google.com/file/d/1cxtB_hTSnTHoa6z3OZ4_vcVrn0AR1BPO/view?usp=sharing](https://drive.google.com/file/d/1cxtB_hTSnTHoa6z3OZ4_vcVrn0AR1BPO/view?usp=sharing)

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Technologies](#technologies)
- [License](#license)
- [Credits](#credits)

## Installation
In order to use this project, the user must have Node.js and MySQL installed on their local machine.

To clone the repository to the local machine, type `git clone git@github.com:kaylab78/ecommerce-backend.git` in the command line interface.

This project requires dotenv, Express.js, MySQL2 and Sequelize. First use `npm init -y` to initialize. Then use `npm install` to install the required packages.

## Usage
To create the schema in the MySQL shell, use the following commands:
```
mysql -u root -p
// You'll be prompted to enter your password
mysql> source db/schema.sql
```

To seed the data in the database, navigate to the CLI and type `npm run seed`.

To start the server and test the API routes, type `node server` or `npm start` in the CLI.

Once the server has started, navigate to Insomnia. Test the following routes.

Category:
- Use a GET route with [http://localhost:3001/api/categories](http://localhost:3001/api/categories) to get all of the categories in the database.
- Use a GET route with an ID to get just one category. Example: [http://localhost:3001/api/categories/1](http://localhost:3001/api/categories/1)
- Use a POST route to create a new category. Use [http://localhost:3001/api/categories](http://localhost:3001/api/categories) with JSON in the body. Example: `{ "category_name" : "Swimwsuits" }`
- Use a PUT route to update a category using the category ID. Example: [http://localhost:3001/api/categories/6](http://localhost:3001/api/categories/6) with JSON body `{ "category_name" : "Swimwear" }`
- Use a DELETE route to delete a category using the ID. Example: [http://localhost:3001/api/categories/6](http://localhost:3001/api/categories/6)

![The screen shows the Insomnia app with example GET, POST, PUT and DELETE routes running successfully.](/assets/screenshot-1.gif)

Tag:
- Use a GET route with [http://localhost:3001/api/tags](http://localhost:3001/api/tags) to get all of the tags in the database.
- Use a GET route with an ID to get just one tag. Example: [http://localhost:3001/api/tags/1](http://localhost:3001/api/tags/1)
- Use a POST route to create a new tag. Use [http://localhost:3001/api/tags](http://localhost:3001/api/tags) with JSON in the body. Example: `{ "tag_name" : "jazz music" }`
- Use a PUT route to update a tag using the tag ID. Example: [http://localhost:3001/api/tags/9](http://localhost:3001/api/tags/9) with JSON body `{ "tag_name" : "summer" }`
- Use a DELETE route to delete a tag using the ID. Example: [http://localhost:3001/api/tags/9](http://localhost:3001/api/tags/9)

![The screen shows the Insomnia app with example GET, POST, PUT and DELETE routes running successfully.](/assets/screenshot-2.gif)

Product:
- Use a GET route with [http://localhost:3001/api/products](http://localhost:3001/api/products) to get all of the products in the database.
- Use a GET route with an ID to get just one product. Example: [http://localhost:3001/api/products/5](http://localhost:3001/api/products/5)
- Use a POST route to create a new product. Use [http://localhost:3001/api/products](http://localhost:3001/api/products) with JSON in the body. Example: 
```
{
    "product_name": "Basketball",
    "price" : 200.00,
    "stock" : 3,
    "tagIds" : [1, 2, 3, 4]
}
```
- Use a PUT route to update a product using the product ID. Example: [http://localhost:3001/api/products/5](http://localhost:3001/api/products/5) with JSON body `{ "product_name": "Camo Cargo Shorts" }`
- Use a DELETE route to delete a product using the ID. Example: [http://localhost:3001/api/products/6](http://localhost:3001/api/products/6)

![The screen shows the Insomnia app with example GET, POST, PUT and DELETE routes running successfully.](/assets/screenshot-3.gif)

## Technologies
- [dotenv](https://www.npmjs.com/package/dotenv)
- [Express.js](https://expressjs.com/)
- [MySQL2](https://www.npmjs.com/package/mysql2)
- [Node.js](https://nodejs.dev/)
- [Sequelize](https://www.npmjs.com/package/sequelize)

## License
&copy; 2022 by Kayla Backus

This project is licensed under the MIT license.

[License: MIT License](https://opensource.org/licenses/MIT)

## Credits
Starter code cloned from Xander Rapstine at [https://github.com/coding-boot-camp/fantastic-umbrella](https://github.com/coding-boot-camp/fantastic-umbrella).

Meg Meyers, boot camp tutor, assisted me with the POST and PUT routes for Product. She discovered that there was a line of code missing from the starter code that made Insomnia return a 400 error when I tried to test the PUT route.