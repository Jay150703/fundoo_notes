# Fundoo Notes 

This project is a Spring Boot based backend application for managing notes with user authentication and advanced backend features. It is designed to follow a clean layered architecture and demonstrate both fundamental and advanced backend development concepts.

---

> **Note:**  
> The complete source code for this project is available in the `dev` branch.  
> The `main` branch contains only project overview and documentation.

---

## Project Overview

Fundoo Notes allows users to create and manage personal notes securely. Each user can perform operations like creating, updating, deleting, and organizing notes using features such as pin, archive, trash, labels, and reminders.

The project is built not just as a basic CRUD application, but as a structured backend system with scalability, performance, and maintainability in mind.

## Core Features

- User registration and login
- Token-based authentication
- Create, read, update, and delete notes
- Pin, archive, and trash notes
- Add labels to notes
- Set reminders for notes
- Search and filter notes
- Global exception handling
- Logging for debugging and monitoring

## Advanced Features

- Asynchronous processing for background tasks (notifications, emails)
- Caching using Redis for improved performance
- Token and OTP storage with expiry
- Batch processing for bulk operations (import/export, cleanup)
- AOP for logging and performance tracking
- Basic microservices readiness using Spring Cloud concepts

## Tech Stack

- Spring Boot
- Spring Web (REST APIs)
- Spring Data JPA (ORM)
- MySQL (Database)
- Redis (Caching)
- RabbitMQ / JMS (Messaging)
- Spring Batch
- Spring AOP

## Architecture

The application follows a layered architecture:

Controller → Handles HTTP requests  
Service → Contains business logic  
Repository → Interacts with the database  

Additional layers:
- DTOs for request/response handling
- Exception handling for consistent error responses
- Security for authentication
- AOP for cross-cutting concerns

## Workflow Example

### User Registration
- User sends registration request
- Data is validated and stored in database
- Token is generated
- Background task is triggered for email/notification

### Note Creation
- Request is validated
- Note is saved in database
- Cache is updated or cleared

### Reminder Handling
- Reminder is stored
- Event is published
- Background service processes notification

## How to Run

1. Clone the repository
2. Open the project in IntelliJ or VS Code
3. Configure database in `application.properties` or `application.yml`
4. Run the Spring Boot application
5. Test APIs using Postman

## Learning Focus

This project helps in understanding:

- How a real backend system is structured
- How to separate responsibilities using layers
- How authentication and token flow works
- How caching improves performance
- How asynchronous systems work
- How to design scalable backend applications

## Future Enhancements

- Frontend integration (React)
- Full Spring Security implementation (JWT, OAuth2)
- API Gateway and microservices setup
- Notification system (Email/SMS)
- File upload support

## Conclusion

Fundoo Notes is a complete backend project that combines core backend development with advanced concepts. It provides a strong foundation for building scalable and production-ready applications using Spring Boot.
