# 📘 Week 02 · ASP.NET Core MVC (Part 1 of 3)

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. MVC

> 💡 This week connects the concepts you learned earlier.
>
> Instead of learning MVC and EF Core separately, practice using them together to build a real application.

## 🔗 Resources

- 🎥 [ITI Recordings — videos 4 to 9](https://youtube.com/playlist?list=PLNFDrRZdysFzmzqno6G1EoxhIKo5sKiwL)
- 🎥 [Coding Future — videos 21 to 36](https://youtube.com/playlist?list=PLPZvv4Sjz6uHtXszCb132o7Oe_T_ur2FP)
- 🎥 [Codographia](https://www.youtube.com/playlist?list=PLX1bW_GeBRhAjpkPCTpKXJoFGe2ZpYGUC)
- 🎥 [Ahmed Mohamady](https://www.youtube.com/playlist?list=PLqPejUavRNTWqGYP-f1pHkbLYdbqi_Uhg)

## 📝 Assignment
- [ ] Student Management System (ASP.NET Core MVC)

Upgrade your existing Student Management project by adding Course management using Entity Framework Core with SQL Server. Configure ApplicationDbContext and apply Code-First migrations to generate the database. Implement full CRUD operations for Courses and link each Student to a specific Course.

- Create a Course model with CourseId, CourseName, CourseCode, Credits, and Description.
- Update the Student model to include CourseId as a foreign key and a navigation property.
- Build a CourseController with Index(), Details(id), Create(), Edit(id), and Delete(id).
- Update the Student Create/Edit views to include a course dropdown list and show course information in the Student Details page.

---

<div align="center">

[⬅️ Previous](week-01.md) · [🏠 Level overview](README.md) · [Next ➡️](week-03.md)

</div>
