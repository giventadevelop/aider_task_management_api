# Task Management API

## Overview

This is a Task Management API built with Spring Boot. It provides a RESTful interface for managing tasks, allowing users to create, read, update, and delete tasks.

## Technologies Used

- Java 17
- Spring Boot 3.2.0
- Spring Data JPA
- H2 Database (in-memory)
- Maven
- SpringDoc OpenAPI (for API documentation)

## Project Structure

The project follows a standard Spring Boot application structure:

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── example
│   │           └── taskmanagement
│   │               ├── controller
│   │               ├── model
│   │               ├── repository
│   │               ├── service
│   │               └── TaskManagementApplication.java
│   └── resources
└── test
    └── java
        └── com
            └── example
                └── taskmanagement
                    └── service
```

## Main Components

1. **Model**: The `Task` class represents the task entity with properties like id, title, description, and completion status.

2. **Repository**: `TaskRepository` extends JpaRepository to provide CRUD operations for the Task entity.

3. **Service**: 
   - `TaskService` interface defines the business logic operations.
   - `TaskServiceImpl` implements these operations using the repository.

4. **Controller**: `TaskController` exposes RESTful endpoints for task management.

5. **Application**: `TaskManagementApplication` is the main class that bootstraps the Spring Boot application.

## Building and Running the Application

1. Ensure you have Java 17 and Maven installed on your system.

2. Clone the repository:
   ```
   git clone <repository-url>
   cd task-management-api
   ```

3. Build the project:
   ```
   mvn clean install
   ```

4. Run the application:
   ```
   mvn spring-boot:run
   ```

The application will start and be available at `http://localhost:8080`.

## API Documentation

Once the application is running, you can access the API documentation:

- Swagger UI: http://localhost:8080/swagger-ui.html
- OpenAPI JSON: http://localhost:8080/v3/api-docs

## Testing

To run the tests, execute:

```
mvn test
```

## API Endpoints

- GET /api/tasks - Retrieve all tasks
- GET /api/tasks/{id} - Retrieve a specific task
- POST /api/tasks - Create a new task
- PUT /api/tasks/{id} - Update an existing task
- DELETE /api/tasks/{id} - Delete a task

For detailed request/response formats, please refer to the Swagger UI documentation.
