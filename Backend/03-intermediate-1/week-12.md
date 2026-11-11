# 📘 Week 12 · EF Core Advanced

> **Track:** Backend  ·  **Level:** 🚀 Intermediate 1

## 📚 Topics
1. EF Core

> 💡 You don't need to know every advanced EF Core feature yet. The goal is to understand how to work with real-world relationships and retrieve data efficiently.

## 🔗 Resources

- 🎥 [DevCreed — videos 54 to 70](https://www.youtube.com/playlist?list=PL62tSREI9C-cHV28v-EqWinveTTAos8Pp)
- 🎥 [Metigator](https://www.youtube.com/playlist?list=PL4n1Qos4Tb6QZkbTWJx7wHqEABP8Pg6uv)
- 🎥 [ITI Recordings](https://www.youtube.com/playlist?list=PLYxGWFnJFttTXpjYdXbkYf5Gsi3AH9o0U)

## 📝 Assignment
- [ ] Employee & Project Management System (EF Core Advanced)

Continue working on the **Employee & Project Management System** from Week 11. Extend the existing application by adding relationships between entities and retrieving related data using Entity Framework Core.

**1. Define Entity Relationships**

- **Department – Employee:** One department can have multiple employees, and each employee belongs to one department.
- **Employee – Project:** An employee can participate in multiple projects, and each project can have multiple employees.

**2. Manage Relationships**

- Assign an employee to a department.
- Change an employee's department.
- Assign employees to projects.
- Remove employees from projects.

**3. Display Related Data**

- Display employee details, including their department and projects.
- Display department details, including its employees.
- Display project details, including its employees.
- Use navigation properties and `Include()` to retrieve related data where appropriate.

**4. Update the Database**

- Add the required foreign keys and navigation properties.
- Create and apply new migrations to update the existing database schema.

**5. Handle User Interaction**

- When editing a record, display its existing data before asking for changes.
- Do not expose database IDs as the choices users must select. Display numbered options or names instead.
- Handle invalid selections and prevent deleting entities when doing so would leave invalid relationships.

---

<div align="center">

[⬅️ Previous](week-11.md) · [🏠 Level overview](README.md) · [Next ➡️](week-13.md)

</div>
