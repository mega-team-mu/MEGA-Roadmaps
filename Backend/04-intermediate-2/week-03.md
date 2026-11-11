# 📘 Week 03 · ASP.NET Core MVC (Part 2 of 3)

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. MVC

> 💡 The goal is not to memorize every MVC feature.
>
> Focus on understanding how to structure a real application and how different ASP.NET Core components communicate with each other.

## 🔗 Resources

- 🎥 [ITI Recordings — videos 10 to 15](https://youtube.com/playlist?list=PLNFDrRZdysFzmzqno6G1EoxhIKo5sKiwL)
- 🎥 [Coding Future — videos 39 to 43 & 50 & 53 to 56 & 60 to 68](https://youtube.com/playlist?list=PLPZvv4Sjz6uHtXszCb132o7Oe_T_ur2FP)
- 🎥 [Codographia](https://www.youtube.com/playlist?list=PLX1bW_GeBRhAjpkPCTpKXJoFGe2ZpYGUC)
- 🎥 [Ahmed Mohamady](https://www.youtube.com/playlist?list=PLqPejUavRNTWqGYP-f1pHkbLYdbqi_Uhg)

## 📝 Assignment
- [ ] Student Management System — Validation & Repository Pattern

Refactor the existing **Student Management System** to use **clean architecture**, proper **validation**, and **Dependency Injection** using the **Repository Pattern**.

**1. Validation**

**Update Student Model with Data Annotations:**

- Name => Required & StringLength(50, MinimumLength = 3)
- Email => Required & EmailAddress
- Age => Range(18, 60)

**Views:**

- Ensure the "Create" and "Edit" views render validation messages ().
- Enable Client-Side Validation so the form validates immediately without reloading the page.

**Custom Validation:**

- Create a custom attribute `[UniqueEmail]` to prevents duplicate emails in the database

**2. Refactoring Repository Pattern Architecture**

**Create Repository Interface `IStudentRepository` with methods:**

- GetAll()
- GetById(int id)
- Add(Student s)
- Update(Student s)
- Delete(int id)

**Implement Repository `StudentRepository`:**

- Implements `IStudentRepository`
- Uses `AppDbContext`

**Refactor Controller:**

- Remove direct dependency on `AppDbContext`
- Inject `IStudentRepository` via constructor
- Use repository methods for all CRUD operations

**Dependency Injection Configuration:**

- Register `StudentRepository` in Program.cs with Scoped lifetime :

**Bonus: State Management**

- Store IDs of recently visited students in Session
- On Index page:
    - Display **last 3 viewed students**
    - Section title: *Recently Viewed*

---

<div align="center">

[⬅️ Previous](week-02.md) · [🏠 Level overview](README.md) · [Next ➡️](week-04.md)

</div>
