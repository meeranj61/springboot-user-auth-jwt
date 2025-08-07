# Spring Boot Authentication API

This project provides a simple User Authentication API using Spring Boot, Spring Security, JWT, and MySQL.

## Features
- User Registration (`/api/auth/register`)
- User Login (`/api/auth/login`) returns JWT token
- Get Current User Info (`/api/user/me`) requires Bearer token

## Requirements
- Java 17+
- Maven
- MySQL (XAMPP)

## Setup
1. Create a MySQL database `auth_db`
2. Update `application.properties` if needed
3. Run the project:
   ```bash
   mvn spring-boot:run
   ```

## API Testing (Postman)
### Register
POST http://localhost:8080/api/auth/register
```json
{
  "username": "syed",
  "email": "syed@test.com",
  "password": "123456"
}
```

### Login
POST http://localhost:8080/api/auth/login
```json
{
  "username": "syed",
  "password": "123456"
}
```
Response: JWT Token

### Get User Info
GET http://localhost:8080/api/user/me
Headers:
```
Authorization: Bearer <JWT_TOKEN>
```
