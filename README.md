Explanation:
Product Entity: Represents the Product entity with id, name, pricePerUnit, and activeForSell attributes. Annotated with @Entity for JPA entity mapping.

ProductRepository: Interface extending JpaRepository to perform CRUD operations on Product entities. Spring Data JPA provides implementations of these methods at runtime.

ProductController Class:

Annotated with @RestController to indicate it's a controller for RESTful endpoints.
Defines @PostMapping, @GetMapping, @PutMapping annotations to handle HTTP POST, GET, PUT requests for /products endpoint and its variations (/products/{id}).
Uses @Autowired to inject ProductRepository dependency for database operations.
Endpoints:

POST /products: Adds a new product (addProduct method).
GET /products/{id}: Retrieves a product by ID (getProductById method).
GET /products: Retrieves all products (getAllProducts method).
PUT /products/{id}: Updates an existing product by ID (updateProduct method).
Running the Application:
Ensure your MySQL database is running and update application.properties (or application.yml) with your database configuration (spring.datasource.url, spring.datasource.username, spring.datasource.password).

Run the Spring Boot application (main method in your main class annotated with @SpringBootApplication).

Use tools like Postman or curl to test the endpoints:

POST http://localhost:8080/products with JSON body to add a new product.
GET http://localhost:8080/products/{id} to retrieve a product by ID.
GET http://localhost:8080/products to retrieve all products.
PUT http://localhost:8080/products/{id} with JSON body to update a product by ID.
