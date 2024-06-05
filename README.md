
# E-Commerce Minimal API

This project is for an e-commerce system, built with ASP.NET Core 7 Minimal APIs and Entity Framework Core. It provides CRUD operations for managing products and categories.

## Features

- CRUD operations for Products and Categories
- Filtering products by price or category
- Searching products by name or description
- Aggregated data endpoints: average price of all products, total number of products in each category

## Technologies Used

- ASP.NET Core 7
- Entity Framework Core
- SQL Server (or LocalDB for development)

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/ecommerce-system-api.git
   cd ecommerce-system-api
   ```

2. **Configure the database:**
   - Update the connection string in `appsettings.json`:
     ```json
     "ConnectionStrings": {
       "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=YourDatabaseName;Trusted_Connection=True;MultipleActiveResultSets=true"
     }
     ```

3. **Apply migrations:**
   ```bash
   dotnet ef database update
   ```

4. **Run the application:**
   ```bash
   dotnet run
   ```

## Endpoints

### Product Endpoints
- **Create Product:** `POST /products`
- **Get All Products:** `GET /products`
- **Get Product By ID:** `GET /products/{id}`
- **Update Product:** `PUT /products/{id}`
- **Delete Product:** `DELETE /products/{id}`
- **Filter Products by Price:** `GET /products/filter?minPrice={minPrice}&maxPrice={maxPrice}`
- **Filter Products by Category:** `GET /products/category/{categoryId}`
- **Search Products:** `GET /products/search?query={query}`
- **Average Price of Products:** `GET /products/average-price`
- **Total Products by Category:** `GET /products/category-count`

### Category Endpoints
- **Create Category:** `POST /categories`
- **Get All Categories:** `GET /categories`
- **Get Category By ID:** `GET /categories/{id}`
- **Update Category:** `PUT /categories/{id}`
- **Delete Category:** `DELETE /categories/{id}`

## Testing

Use tools like Postman or Swagger to test the API endpoints.

## Additional Information

This project demonstrates good practices in code organization and separation of concerns by using a service layer to handle business logic.
