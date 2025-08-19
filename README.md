# Spring Boot RESTful Web Services

A production-ready RESTful web service built with Spring Boot that demonstrates best practices in API development, including DTO pattern implementation, comprehensive exception handling, request validation, and API documentation.

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

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [Spring Boot](https://spring.io/projects/spring-boot)
- [MapStruct](https://mapstruct.org/)
- [ModelMapper](http://modelmapper.org/)
- [SpringDoc OpenAPI](https://springdoc.org/)
