## How to Run the Code

1. Ensure you have the following prerequisites installed:
   - Java Development Kit (JDK) 23
   - Maven
   - MySQL

2. Clone the repository to your local machine.

3. Navigate to the project root directory.

4. Configure the database connection in `src/main/resources/application.properties`:
spring.datasource.url=jdbc:mysql://localhost:3306/category_product
spring.datasource.username=your_username
spring.datasource.password=your_password

Replace `your_username` and `your_password` with your MySQL credentials.

5. Create a database named `category_product` in MySQL.

6. Build the project using Maven:
   
7. Run the application:

8. The application should now be running on `http://localhost:8080`.

## How to Run the Machine Test

To test the API endpoints, I used tool Postman.

1. Create a Category (POST):
POST http://localhost:8080/api/categories
Body: {"name": "Electronics"}


2. Get all Categories (GET):
   GET http://localhost:8080/api/categories?page=0]


3. Get Category by ID (GET):
GET http://localhost:8080/api/categories/{id}


4. Update Category (PUT):
PUT http://localhost:8080/api/categories/{id}
Body: {"name": "Machines"}


5. Delete Category (DELETE):
DELETE http://localhost:8080/api/categories/{id}


6. Create a Product (POST):
   POST http://localhost:8080/api/products
Body: {
"name": "Smartphone",
"description": "Latest model smartphone",
"price": 999.99,
"category": {
"id": 1
}
}



7. Get all Products (GET):
   GET http://localhost:8080/api/products?page=0



8. Get Product by ID (GET):
GET http://localhost:8080/api/products/{id}


9. Update Product (PUT):
PUT http://localhost:8080/api/products/{id}
Body: {
"name": "Updated Smartphone",
"description": "Latest model smartphone with new features",
"price": 1099.99,
"category": {
"id": 1
}
}


10. Delete Product (DELETE):
 DELETE http://localhost:8080/api/products/{id}
