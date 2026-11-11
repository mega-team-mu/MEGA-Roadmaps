# 📘 Week 05 · ASP.NET Core API (Part 1 of 3)

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. API

> 💡 The goal of this week is to understand how a Backend API works and how clients communicate with it through HTTP.
>
> Focus on understanding the request/response flow rather than memorizing API syntax.

## 🔗 Resources

- 🎥 [Passionate Coders — videos 1 to 4](https://www.youtube.com/playlist?list=PLsV97AQt78NQ8E7cEqovH0zLYRJgJahGh)
- 🎥 [ITI Recordings — videos 1 to 2](https://youtube.com/playlist?list=PLoRh0POuk1RyWlnOvUtDvRQ1aTmz69W8L)
- 📁 [مبادرة رودا مصر الرقمية](https://drive.google.com/drive/folders/1Ifg6PtZ63XqntLSJnT_jHgxlfa5UypoO) `Arabic`

## 📝 Assignment
- [ ] To-Do Web API (ASP.NET Core)

Build a minimal **To-Do Web API** using **ASP.NET Core Web API**. The goal is to understand how Controllers, Dependency Injection, HTTP methods, status codes, and a Service Layer work together.

**1. Model**

Create a `TodoItem` class with the following properties:

- `Id`: Integer, generated manually by the service.
- `Title`: Required string.
- `IsComplete`: Boolean indicating whether the task is completed.

**2. Service Layer**

- Create an `ITodoService` interface with methods to retrieve all items, retrieve an item by ID, and add a new item.
- Implement `TodoService` using an in-memory `List<TodoItem>`.
- Initialize the list with one sample item.
- Register `ITodoService` in the dependency injection container as a **Singleton**.

**3. Controller**

Create a `TodosController` with the route `api/todos` and inject `ITodoService` through its constructor.

Implement the following endpoints:

- **GET `/api/todos`:** Return all To-Do items with `200 OK`.
- **GET `/api/todos/{id}`:** Return the requested item with `200 OK`, or `404 Not Found` if it does not exist.
- **POST `/api/todos`:** Accept a new item as JSON, generate its ID, add it to the list, and return `201 Created` with the created item and a `Location` header pointing to its details endpoint.

**4. Validation**

- Apply `[ApiController]` to the controller.
- Use `[Required]` to validate the `Title` property.
- Ensure invalid requests receive appropriate validation responses.
- Use ASP.NET Core Web API.
- Use in-memory storage only; **no database or Entity Framework Core**.
- Use constructor injection to access the service.
- Use appropriate HTTP methods and status codes.
- Keep the project structure simple and organized into Models, Services, and Controllers.

---

<div align="center">

[⬅️ Previous](week-04.md) · [🏠 Level overview](README.md) · [Next ➡️](week-06.md)

</div>
