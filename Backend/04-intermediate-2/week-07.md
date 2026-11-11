# 📘 Week 07 · ASP.NET Core API (Part 3 of 3)

> **Track:** Backend  ·  **Level:** 🌐 Intermediate 2

## 📚 Topics
1. API

> 💡 The goal is to move from simply making an API work to building an API that is organized, understandable, and easier to maintain.

## 🔗 Resources

- 🎥 [Passionate Coders — videos 11 to 14](https://www.youtube.com/playlist?list=PLsV97AQt78NQ8E7cEqovH0zLYRJgJahGh)
- 🎥 [ITI Recordings — videos 5 to 6](https://youtube.com/playlist?list=PLoRh0POuk1RyWlnOvUtDvRQ1aTmz69W8L)
- 📁 [مبادرة رودا مصر الرقمية](https://drive.google.com/drive/folders/1Ifg6PtZ63XqntLSJnT_jHgxlfa5UypoO) `Arabic`

## 📝 Assignment
- [ ] Secure Document Management API

Build a **Secure Document Management API** using ASP.NET Core Web API. The goal is to implement JWT Authentication and different authorization mechanisms, including Role-Based, Policy-Based, and Custom Permission-Based Authorization.

**1. Project Setup & User Store**

- Create an ASP.NET Core Web API project.
- Configure JWT Authentication using `Microsoft.AspNetCore.Authentication.JwtBearer`.
- Configure JWT settings, including Issuer, Audience, and Signing Key.
- Create an in-memory user list containing:
    - `Id`
    - `Username`
    - `Password`
    - `Role`
    - `Permissions` (`List<string>`)

**2. Authentication Endpoint**

Create an `AuthController` with the following endpoint:

- **POST `/api/auth/login`:** Accept a username and password, validate the credentials, generate a JWT containing the user's ID, role, and permissions, and return the token.

**3. Custom Permission Authorization**

- Create a custom `[CheckPermission("PermissionName")]` attribute.
- Implement an authorization filter that reads the required permission.
- Extract the user's ID from the JWT.
- Check whether the user has the required permission using the in-memory user store.
- Return `403 Forbidden` when the authenticated user lacks the required permission.

**4. Documents API**

Create a `DocumentsController` with the following endpoints:

| Endpoint | Method | Authorization Requirement |
| --- | --- | --- |
| `/api/documents` | GET | Only users with the Admin or Editor role |
| `/api/documents` | POST | Requires the `CreateDoc` permission |
| `/api/documents/{id}` | PUT | Requires authentication and the `UpdateDoc` permission |
| `/api/documents/{id}` | DELETE | Only an Admin or the document owner |

Use an in-memory collection to store documents. Each document should have an ID, title, content, and owner ID.

**5. Policy-Based Authorization**

- Create a `DocumentOwnerRequirement` class.
- Implement `AuthorizationHandler<DocumentOwnerRequirement>`.
- Register the handler and policy in `Program.cs`.
- Configure the `DocumentOwnerOrAdmin` policy to allow deletion only when the user is an Admin or owns the requested document.

**6. Testing & Error Handling**

- Test the endpoints using Swagger or Postman.
- Verify that unauthenticated requests receive `401 Unauthorized`.
- Verify that authenticated users without sufficient permissions receive `403 Forbidden`.
- Test access with different roles and permissions.
- Handle cases where a document does not exist.

---

<div align="center">

[⬅️ Previous](week-06.md) · [🏠 Level overview](README.md) · [Next ➡️](week-08.md)

</div>
