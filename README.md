# Employee Tracker
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

This project requires dotenv, Express.js, MySQL2 and Sequelize. First use `npm init` to initialize. Then use `npm install` to install the required packages.

To create the schema in the MySQL shell, use the following commands:
```
mysql -u root -p
// You'll be prompted to enter your password
mysql> source db/schema.sql
```

To seed the data in the database, navigate to the CLI and type `npm run seed`.

To start the server and test the API routes, type `node server` or `npm start` in the CLI.

## Usage

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

Meg Meyers, boot camp tutor, assisted me with the POST and PUT routes for Product.