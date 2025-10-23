# 🔐 User Authentication System (Spring Boot + JWT)

A secure backend authentication system built with **Spring Boot**, implementing **JWT-based login**, **user registration**, and **role-based authorization**.

---

## 🚀 Tech Stack
- **Java 21**
- **Spring Boot 3.x**
- **Spring Security**
- **JWT (JSON Web Token)**
- **Spring Data JPA**
- **MySQL**
- **Maven**
- **Lombok**
- **Postman** (for API testing)

---

## 🏗️ Architecture Overview

- **Controllers:** Handle user registration and login requests.  
- **Services:** Business logic for authentication and user management.  
- **Repositories:** JPA interfaces for DB communication.  
- **JWT Layer:** Generates and validates tokens.  
- **Security Config:** Defines access rules for protected endpoints.

---

## 🧩 Features
✅ Register new users with encrypted passwords (BCrypt)  
✅ Login with email/username and password  
✅ JWT token generation and validation  
✅ Role-based access (USER / ADMIN)  
✅ Secured endpoints accessible only with valid tokens  
✅ Clean error handling with Spring’s `@ControllerAdvice`

---

## ⚙️ API Endpoints

### 🔸 Authentication
| Method | Endpoint | Description |
|:------:|-----------|-------------|
| `POST` | `/api/auth/register` | Register new user |
| `POST` | `/api/auth/login` | Authenticate user and return JWT token |

### 🔸 Protected (Example)
| Method | Endpoint | Access |
|:------:|-----------|--------|
| `GET` | `/api/user/profile` | USER / ADMIN |
| `GET` | `/api/admin/dashboard` | ADMIN only |

---

## 🧠 Example JSON Requests

### 🔹 Register
```json
{
  "username": "siva",
  "email": "siva@example.com",
  "password": "password123",
  "role": "USER"
}
###🔹  Login 
{
  "email": "siva@example.com",
  "password": "password123"
}

###🔹 Login Response
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}


