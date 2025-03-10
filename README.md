# API Development Assignment - README  

## Introduction  
This assignment focuses on developing APIs to handle various data entities, including student records, product management, and category organization for an online store. The implementation will leverage both PHP and Laravel frameworks. Below is a detailed breakdown of the activities and their corresponding implementation steps.  

## Activity 1: Representing Student Information (XML and JSON)  
In this task, you will create XML and JSON structures to represent student details, including their name, age, gender, and a list of enrolled subjects. Each subject must include its name and corresponding grade.  

Additionally, you will write XQuery expressions to extract specific data, such as retrieving the student’s name and age, along with the names of all enrolled subjects.  

## Activity 2: Developing a Simple Product Management API (PHP)  
This activity involves building a basic RESTful API in PHP to manage products. The API should support the following endpoints:  

- **GET /products** - Retrieve a list of all products.  
- **GET /products/{id}** - Retrieve a product by its ID.  
- **POST /products** - Add a new product.  
- **PUT /products/{id}** - Modify an existing product using its ID.  
- **DELETE /products/{id}** - Remove a product using its ID.  

Each product should include an ID, name, description, and price. The data will be managed using an array for simplicity, and all API responses should be formatted in JSON.  

## Activity 3: Category Management API for an Online Store (Laravel)  
This task requires setting up a Laravel-based API to manage product categories within an online store. A MySQL database named **online_store** will be created, containing a **categories** table with the following fields: `id`, `name`, `lft`, `rgt`, `created_at`, and `updated_at`.  

To efficiently manage hierarchical categories, Laravel’s Eloquent ORM will be used with the **Nested Set Model**. The API should support the following operations:  

- **GET /categories** - Retrieve all categories in XML format.  
- **GET /categories/{id}** - Fetch a specific category by ID in XML format.  
- **POST /categories** - Add a new category (expects XML input with `name` and `parent_id`).  
- **PUT /categories/{id}** - Modify an existing category (expects XML input with `name`).  
- **DELETE /categories/{id}** - Remove a category and return a success response in XML format.  

Validation and error handling must be implemented, ensuring invalid requests return XML-formatted error messages. Laravel’s routing, controllers, and models will be utilized for this implementation, with unit tests ensuring the API's reliability.  

## Activity 4: API Development for a Banking System (Laravel)  
In this final activity, you will develop a banking system API using Laravel. The system will facilitate basic banking operations such as:  

- Creating user accounts.  
- Making deposits.  
- Processing withdrawals.  

### Prerequisites  
Ensure the following dependencies are installed before proceeding:  

- PHP (version 8.0 or later)  
- Composer  
- MySQL (or another database of choice)  
- Laravel (version 9 or later)  
- Node.js and NPM (for frontend asset management)  

### Installation Instructions  
1. Clone the project repository.  
2. Install backend dependencies:  
   ```bash
   composer install
   ```  
3. Configure the environment file by duplicating `.env.example` and updating database connection details.  
4. Generate an application key:  
   ```bash
   php artisan key:generate
   ```  
5. Run database migrations and seed sample data:  
   ```bash
   php artisan migrate  
   php artisan db:seed  
   ```  
6. Start the Laravel development server:  
   ```bash
   php artisan serve  
   ```  

### Frontend Setup  
To set up the frontend, install dependencies:  
```bash
npm install
```  
Then compile assets:  
```bash
npm run dev
```  

## API Documentation  
The API can be tested using tools such as **Postman** or **Swagger**. The Swagger UI will automatically generate API documentation, accessible through a specified URL.  

## Conclusion  
This assignment provides hands-on experience in API development, covering XML/JSON data handling, building RESTful APIs with PHP, managing hierarchical categories in Laravel, and developing a banking system API. Following these structured steps will ensure the creation of a robust and maintainable API system.

