# 📘 Week 06 · ASP.NET Core API (Part 2 of 3)

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. API

> 💡 This week connects the API layer with the database.
>
> Focus on building APIs that work with real data and returning appropriate responses instead of exposing database entities directly.

## 🔗 Resources

- 🎥 [Passionate Coders — videos 5 to 10](https://www.youtube.com/playlist?list=PLsV97AQt78NQ8E7cEqovH0zLYRJgJahGh)
- 🎥 [ITI Recordings — videos 3 to 4](https://youtube.com/playlist?list=PLoRh0POuk1RyWlnOvUtDvRQ1aTmz69W8L)
- 📁 [مبادرة رودا مصر الرقمية](https://drive.google.com/drive/folders/1Ifg6PtZ63XqntLSJnT_jHgxlfa5UypoO) `Arabic`

## 📝 Assignment
- [ ] Product Management API

Build a **Product Management Web API** using ASP.NET Core Web API and Entity Framework Core. The application should support CRUD operations while demonstrating Dependency Injection, Action Filters, Configuration, Logging, and Model Binding.

**1. Product Management**

- Create a `Product` model with properties such as `Id`, `Name`, `Description`, `Price`, and `Stock`.
- Implement full CRUD operations:
    - **GET:** Retrieve all products or a specific product.
    - **POST:** Create a new product.
    - **PUT:** Update an existing product.
    - **DELETE:** Remove a product.

**2. Database Integration**

- Use Entity Framework Core with SQL Server.
- Create a `DbContext` and configure the database connection.
- Use Code First migrations to create and update the database.
- Ensure product data persists after restarting the application.

**3. Service Layer & Dependency Injection**

- Create a `ProductService` to handle product-related operations.
- Register the service using Dependency Injection.
- Keep business logic separate from the controller.

**4. Action Filters**

- Create at least one custom Action Filter, such as a filter that measures and logs action execution time or validates product prices.

**5. Configuration & Logging**

- Read a configuration value from `appsettings.json` using `IConfiguration`.
- Use `ILogger` to log important actions, such as creating, updating, and deleting products.

**6. Model Binding**

Demonstrate the use of:

- `[FromRoute]` to retrieve a product ID from the route.
- `[FromQuery]` to filter or search products using query parameters.
- `[FromBody]` to receive product data in POST and PUT requests.

**7. API Responses & DTOs**

- Return appropriate HTTP status codes, such as `200 OK`, `201 Created`, `204 No Content`, and `404 Not Found`, where applicable.
- Use DTOs for creating, updating, and returning product data instead of exposing database entities directly.

---

<div align="center">

[⬅️ Previous](week-05.md) · [🏠 Level overview](README.md) · [Next ➡️](week-07.md)

</div>
