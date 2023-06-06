# Back-End-E-Commerce

## Description

The E-commerce Backend is a Node.js application that serves as the backend for an e-commerce website. It provides a set of RESTful APIs for managing products, categories, tags, and product tags. The application utilizes Express.js and Sequelize ORM to handle database operations and supports features like creating, reading, updating, and deleting products, associating tags with products, and fetching products with their associated categories and tags. With its intuitive API routes, the E-commerce Backend simplifies the process of building and managing an e-commerce website's backend infrastructure, making it easier to develop and maintain the server-side functionality.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Routes](#api-routes)
- [Database](#database)
- [Contributing](#contributing)
- [License](#license)

## Installation

To install and run the project, please follow the instructions below:

1. Ensure you have Node.js installed on your machine. You can download it from the official Node.js website: https://nodejs.org

2. Clone the project repository from the GitHub repository using the following command:

   git clone <repository_url>

3. Navigate to the project directory:

   cd <project_directory>

4. Install the project dependencies by running the following command:

   npm install

5. Configure the database connection:
   Open the config/connection.js file.
   Modify the database configuration according to your database setup (e.g., database name, username, password).

6. Start the application by running the following command:

   node server.js

7. The server should now be running. You can access the application by opening a web browser and navigating to http://   localhost:3001.

## Usage

1. After successfully installing and running the application, open Insomnia or any other API testing tool.

2. Make sure you have the application's server running. Use the command node server.js to start the server.

3. In Insomnia, create a new request and set the request method and URL to interact with the different endpoints of the   
   application's API.

4. Use the available endpoints to perform various actions. For example:

To retrieve all products, send a GET request to http://localhost:3001/api/products.

To retrieve a specific product, send a GET request to http://localhost:3001/api/products/:id, replacing :id with the actual product ID.

To create a new product, send a POST request to http://localhost:3001/api/products with the required data in the request body.

To update a product, send a PUT request to http://localhost:3001/api/products/:id, replacing :id with the actual product ID, and provide the updated data in the request body.

To delete a product, send a DELETE request to http://localhost:3001/api/products/:id, replacing :id with the actual product ID.

Similarly, you can use the available endpoints for categories, tags, and product tags to perform actions related to those entities.

Test the different endpoints, observe the responses, and verify that the desired actions are being performed correctly.

## API Routes

The application's API provides the following routes for interacting with the data:

GET /api/products: Retrieve all products, including associated category and tag data.
GET /api/products/:id: Retrieve a specific product by its ID, including associated category and tag data.
POST /api/products: Create a new product. Provide the product details in the request body, including product_name, price, stock, and category_id. Optionally, you can include an array of tagIds to associate tags with the product.
PUT /api/products/:id: Update an existing product by its ID. Provide the updated product details in the request body, including product_name, price, stock, and category_id. To update the associated tags, include an array of tags containing the tag IDs. Existing tags not included in the array will be removed, and new tags will be added.
DELETE /api/products/:id: Delete a product by its ID.
GET /api/categories: Retrieve all categories.
GET /api/categories/:id: Retrieve a specific category by its ID, including associated products.
POST /api/categories: Create a new category. Provide the category name in the request body.
PUT /api/categories/:id: Update an existing category by its ID. Provide the updated category name in the request body.
DELETE /api/categories/:id: Delete a category by its ID. This will also delete all associated products.
GET /api/tags: Retrieve all tags.
GET /api/tags/:id: Retrieve a specific tag by its ID, including associated products.
POST /api/tags: Create a new tag. Provide the tag name in the request body.
PUT /api/tags/:id: Update an existing tag by its ID. Provide the updated tag name in the request body.
DELETE /api/tags/:id: Delete a tag by its ID. This will remove the tag association from all products.

## Database

The application utilizes a MySQL database to store and manage data. The database is structured with multiple tables, including products, categories, and tags. The products table stores information about various products, such as their names, prices, and stock availability. The categories table contains the different categories to which the products belong, allowing for categorization and organization. The tags table stores descriptive tags associated with the products, providing additional attributes for classification and searching. These tables work together to form a cohesive database schema, enabling efficient storage and retrieval of data related to products, categories, and tags.

## Contributing

Contributions to the application are welcome and encouraged! If you wish to contribute to the project, please follow these steps:

1. Fork the repository and create a new branch for your feature or bug fix.
2. Make your modifications and ensure that the code adheres to the project's style and guidelines.
3. Write tests to validate the changes and ensure that the existing tests pass successfully.
4. Submit a pull request, providing a clear description of your changes and the problem they solve.
5. Engage in any necessary discussions or iterations to refine your contribution.
6. Once approved, your changes will be merged into the main codebase and become part of the application.

By contributing to the project, you can help enhance its functionality, improve its performance, and fix issues. Your contributions can have a positive impact on the overall quality and usability of the application. Thank you for considering contributing to this project!

## License

MIT

## Demonstration Video Link

https://drive.google.com/file/d/1Kg32_ygj6H-NUeIjtuYa2GKX5f4P2GxP/view

