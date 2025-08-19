# Spring Boot RESTful Web Services

A production-ready RESTful web service built with Spring Boot that demonstrates best practices in API development, including DTO pattern implementation, comprehensive exception handling, request validation, and API documentation.

This repository ([simple-springboot-restful-webservices](https://github.com/Sangramjit786/simple-springboot-restful-webservices.git)) contains a **Spring Boot-based REST API project** that demonstrates best practices for building structured, maintainable, and production-ready web services.  

The project emphasizes the use of **DTO patterns, object mapping frameworks, centralized exception handling, validation, monitoring, and API documentation**.

---

## Project Overview

The project provides a REST API backend showcasing how to build **scalable and clean web services** in Spring Boot.  

It covers the following:
- DTO (Data Transfer Object) implementation for decoupling layers.  
- Object mapping using **ModelMapper** and **MapStruct**.  
- Comprehensive **exception handling** (custom + global).  
- **Validation** of REST API requests with customized error messages.  
- Production-ready monitoring with **Spring Boot Actuator**.  
- API documentation with **SpringDoc OpenAPI** and Swagger UI.

---

## Key Features

### 1. DTO Pattern with ModelMapper and MapStruct
- Implemented the **DTO (Data Transfer Object)** pattern to separate domain models from external representations.
- Implemented the **Data Transfer Object (DTO) pattern** to separate internal domain models from exposed API responses and requests.  
- Ensures **data encapsulation**, prevents leaking domain logic, and provides flexibility in shaping API responses.

#### Object Mapping with ModelMapper and MapStruct
- **ModelMapper**: Used for **runtime object mapping**, allowing quick conversion between entities and DTOs.  
- **MapStruct**: Added as a **compile-time code generator** for high-performance and type-safe mappings.  
- This dual implementation highlights **two common mapping strategies** in modern Spring Boot applications.

This ensures:
- A clean separation between **API layer** and **domain models**.  
- **Performance optimization** using MapStruct’s code generation.  
- Easy maintainability and scalability when DTOs evolve separately from entities.

---

### 2. Exception Handling (Custom + Global)
- Created **custom exception classes** for business-specific errors (e.g., `UserNotFoundException`).  
- Used a **global exception handler** with `@ControllerAdvice` and `@ExceptionHandler` to centralize error handling.  
- Returned **consistent JSON error responses** across all controllers.

This prevents repetitive error handling logic and ensures **clear communication of errors** to API clients.

**Example:**
```json
{
  "timestamp": "2025-08-19T10:00:00",
  "status": 404,
  "error": "Not Found",
  "message": "User with ID 10 not found",
  "path": "/api/v1/users/10"
}
```
---

### 3. Validation of REST API Requests
- Applied **validation annotations** (`@NotNull`, `@Size`, `@Email`, etc.) in DTO classes.  
- Implemented **custom validation messages** to provide meaningful feedback to clients.  
- Designed a **customized error response format** for validation errors, improving usability.
- This ensures clients receive clear, actionable error messages.

This makes the APIs **robust, user-friendly, and self-explanatory** for clients.

**Example:**
```json
{
  "errors": [
    { "field": "email", "message": "must be a valid email address" },
    { "field": "name", "message": "must not be empty" }
  ]
}
```

---

### 4. Spring Boot Actuator Integration
- Enabled **Spring Boot Actuator** to monitor and manage the application in production.  
- Provided endpoints like:
  - `/actuator/health` – Application health status.  
  - `/actuator/info` – Custom application information.
  - `/actuator/metrics` → Application metrics
- Useful for **DevOps teams** to monitor service status and performance.

---

### 5. API Documentation with SpringDoc OpenAPI (Swagger UI)
- Integrated **SpringDoc OpenAPI** to automatically generate API documentation.  
- Swagger UI provides:
  - **Interactive API exploration**.  
  - Ability to **test endpoints directly** from the browser.  
- Enhanced with **annotations** (`@Operation`, `@ApiResponse`, etc.) for clarity and usability.
- Customized documentation with annotations such as:
  - @Operation for endpoint descriptions
  - @ApiResponse for response codes
  - @Parameter for input details
    
**Swagger UI available at:**
```bash
http://localhost:8080/swagger-ui.html
```
This ensures developers and API consumers can easily **understand and test the REST APIs**.

---

## ✨ Features

- **RESTful API Endpoints** for CRUD operations on User resources
- **DTO Pattern** implementation using both ModelMapper and MapStruct
- **Comprehensive Exception Handling** with custom exceptions and global exception handler
- **Request Validation** with meaningful error responses
- **Spring Boot Actuator** for application monitoring and metrics
- **API Documentation** with SpringDoc OpenAPI and Swagger UI
- **Database Integration** with Spring Data JPA and MySQL

## 🛠️ Technologies Used

- **Java 21**
- **Spring Boot 3.5.0**
- **Spring Data JPA**
- **MySQL Database**
- **Lombok** for reducing boilerplate code
- **ModelMapper** for object mapping
- **MapStruct** for compile-time object mapping
- **Spring Validation** for request validation
- **Spring Boot Actuator** for production-ready features
- **SpringDoc OpenAPI** for API documentation

## 🚀 Getting Started

### Prerequisites

- Java 21 or later
- Maven 3.6.3 or later
- MySQL 8.0 or later

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Sangramjit786/simple-springboot-restful-webservices.git
   cd simple-springboot-restful-webservices
   ```

2. **Configure Database**
   - Create a MySQL database named `user_management`
   - Update the database configuration in `src/main/resources/application.properties`
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/user_management
     spring.datasource.username=your_username
     spring.datasource.password=your_password
     ```

3. **Build and Run**
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

## 📚 API Documentation

Once the application is running, you can access the following:

- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **OpenAPI Documentation**: http://localhost:8080/v3/api-docs

## 🎯 API Endpoints

### User Management

|
 Method 
|
 Endpoint 
|
 Description 
|
|
--------
|
----------
|
-------------
|
|
 POST   
|
 /api/users 
|
 Create a new user 
|
|
 GET    
|
 /api/users/{id} 
|
 Get user by ID 
|
|
 GET    
|
 /api/users 
|
 Get all users 
|
|
 PUT    
|
 /api/users/{id} 
|
 Update user 
|
|
 DELETE 
|
 /api/users/{id} 
|
 Delete user 
|

## 🛡️ Exception Handling

The application includes comprehensive exception handling with:

- Custom exceptions (e.g., `ResourceNotFoundException`)
- Global exception handler for consistent error responses
- Validation error handling with detailed error messages

## 🔍 Monitoring

Spring Boot Actuator is configured and can be accessed at:
- http://localhost:8080/actuator

## 📝 DTO Pattern Implementation

The project demonstrates two approaches to DTO mapping:
1. **ModelMapper** - For runtime object mapping
2. **MapStruct** - For compile-time object mapping with better performance

## Learning Outcomes

By working with this project, developers will learn:

- How to implement DTOs with ModelMapper and MapStruct.
- How to handle exceptions consistently and globally in Spring Boot.
- How to validate requests and return structured error responses.
- How to integrate Spring Boot Actuator for production monitoring.
- How to generate interactive API docs with SpringDoc OpenAPI.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [Spring Boot](https://spring.io/projects/spring-boot)
- [MapStruct](https://mapstruct.org/)
- [ModelMapper](http://modelmapper.org/)
- [SpringDoc OpenAPI](https://springdoc.org/)
