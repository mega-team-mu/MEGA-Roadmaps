# 📘 Week 08 · API Security with JWT Tokens & Refresh Tokens

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. Jwt Tokens
2. Jwt Refresh Tokens

> 💡 Focus on understanding what happens when a user logs in, how a JWT is generated, what information it contains, and how the API uses it to identify and authorize the user.
>
> The goal is to understand how authentication is handled beyond a basic JWT implementation, and how APIs can evolve while remaining maintainable for their clients.

## 🔗 Resources

- 🎥 [Jwt Token](https://www.youtube.com/playlist?list=PL62tSREI9C-eYNE1Pyw0yv1tETs5V8WGd)
- 🎥 [Jwt Refresh Token](https://youtube.com/playlist?list=PL62tSREI9C-foV0zXVpW_f0JNtTD6Wv2W)

## 📝 Assignment
- [ ] Extended: Advanced Secure Document Management API

**Objective: Upgrade the foundational Secure Document Management API by implementing Entity Framework Core, Refresh Tokens and an Audit Logging middleware.**

**1. Enhanced Security: Refresh Token Flow**

- **Update AuthController:** Modify the `/login` endpoint to return two tokens:
    - A short-lived JWT Access Token (e.g., expires in 15 minutes).
    - A securely generated, long-lived Refresh Token (e.g., expires in 7 days).
- **Database Storage:** Save the generated Refresh Token to the database, associated with the specific User ID, along with its expiration date.
- **New Endpoint:** Create a `POST /refresh` endpoint that accepts an expired Access Token and a valid Refresh Token, validates them against the database, and issues a fresh pair if valid.

**2. Advanced Authorization (Resource-Based & Departmental)**

- **Department Claims:** Add a "Department" property to the User entity (e.g., "Cardiology", "HR", "IT"). Include this as a claim in the JWT payload.
- **Enhanced Policy:** Update the `PUT /documents/{id}` endpoint. Create a new `DepartmentAccessRequirement` and handler.
    - *Rule:* A user can only update a document if their JWT "Department" claim matches the "Department" tagged on the Document in the database.

**3. Action Filter: Audit Logging**

- **Create an `[AuditLog]` Custom Action Filter:** * Apply this filter to all POST, PUT, and DELETE document endpoints.
    - The filter should intercept the request, extract the UserId from the JWT, and log the action (e.g., "User 104 deleted Document 55") to a new `AuditLogs` database table.

---

<div align="center">

[⬅️ Previous](week-07.md) · [🏠 Level overview](README.md) · [Next level: Advanced ➡️](../05-advanced/README.md)

</div>
