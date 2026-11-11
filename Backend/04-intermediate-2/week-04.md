# 📘 Week 04 · ASP.NET Core MVC (Part 3 of 3)

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. MVC
2. Identity

> 💡 Authentication answers **"Who are you?"**
>
> Authorization answers **"What are you allowed to do?"**
>
> Make sure you understand the difference and practice both in a real application.

## 🔗 Resources

- 🎥 [ITI Recordings — videos 16 to 19](https://youtube.com/playlist?list=PLNFDrRZdysFzmzqno6G1EoxhIKo5sKiwL)
- 🎥 [Coding Future — videos 69 to 85](https://youtube.com/playlist?list=PLPZvv4Sjz6uHtXszCb132o7Oe_T_ur2FP)
- 🎥 [Codographia](https://www.youtube.com/playlist?list=PLX1bW_GeBRhAjpkPCTpKXJoFGe2ZpYGUC)
- 🎥 [Ahmed Mohamady](https://www.youtube.com/playlist?list=PLqPejUavRNTWqGYP-f1pHkbLYdbqi_Uhg)

## 📝 Assignment
- [ ] Secure Student Management System

**Project: Secure Student Management System**

Upgrade your existing Student Management System (which currently uses the Repository Pattern and Validation) to implement Authentication and Authorization using ASP.NET Core Identity.The goal is to secure the application so that only authorized users can manage students and courses.

**Requirements:**

**1. Authentication (User Accounts)**

- **Account Controller:** Create an AccountController with the following actions and views:

  - Register: Allows new users to create an account (Email, Password, Confirm Password).

  - Login: Allows users to sign in.

  - Logout: Signs the user out.

- **UI Update:** Update the _Layout.cshtml navigation bar to:

  - Show "Register" and "Login" links for anonymous users.

  - Show "Logout" and the username (e.g., "Welcome, [User]!") for logged-in users.

**2. Authorization (Role-Based Access Control)**

- **Role Management:** Implement a mechanism to handle Roles (e.g., via a seed method or a simple controller).
- **Create Two Roles:**

1. "Admin": Has full access to the system.

2. "User": Has read-only access.

- **Secure Student & Course Controllers:**

  - Apply the [Authorize] attribute globally or to specific controllers.

  - Admins: Can perform all CRUD operations (Create, Edit, Delete) on Students and Courses.

  - Users: Can only view the Index and Details pages. They should be restricted from accessing Create/Edit/Delete actions.
  - Anonymous (Not Logged In): Should be redirected to the Login page if they try to access any Student or Course pages.

**3. Maintain Existing Architecture**

- Ensure that your existing Repository Pattern implementation (StudentRepository, IStudentRepository) remains intact and functional within the secure environment.
- Ensure that your Validation logic (Data Annotations and Client-Side Validation) continues to work on the forms.

**4. Bonus: User-Specific Logic**

- Modify the Create Student process so that the "CreatedBy" field (if you add one to the model) automatically records the email of the currently logged-in Admin.

**Submission:** Submit the complete project as a **GitHub repository**. The repository must include:
- The updated ApplicationDbContext with Identity.
- The AccountController and associated Views.
- The secured StudentController and CourseController using the Repository Pattern.
- All migrations required to create the Identity tables

---

<div align="center">

[⬅️ Previous](week-03.md) · [🏠 Level overview](README.md) · [Next ➡️](week-05.md)

</div>
