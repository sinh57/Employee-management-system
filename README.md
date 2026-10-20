# Employee Management System

A full-stack Employee Management System built with **Java, Spring Boot, React, and MySQL**. The application allows users to manage employee records through a REST API and a responsive web interface.

## Tech Stack

**Backend**
- Java 17
- Spring Boot 3
- Spring Data JPA and Hibernate
- MySQL
- Maven
- Bean Validation

**Frontend**
- React 18
- Axios
- CSS

**Testing and Database**
- JUnit
- H2 in-memory database

## Features

- Create, view, update, and delete employee records
- Search employees by name
- Filter employees by department
- Validate employee information, including email and salary
- Handle exceptions with meaningful error responses
- RESTful API using standard HTTP methods
- Separate frontend and backend architecture

## Project Structure

```text
employee-management-system/
├── backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/ems/employeemanagement/
│   │   │   │   ├── controller/
│   │   │   │   ├── entity/
│   │   │   │   ├── exception/
│   │   │   │   ├── repository/
│   │   │   │   └── service/
│   │   │   └── resources/
│   │   └── test/
│   ├── Dockerfile
│   └── pom.xml
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── services/
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── package-lock.json
├── .gitignore
└── README.md
```

## Prerequisites

Install the following before running the application:

- Java 17 or later
- Maven
- Node.js and npm
- MySQL, if using the MySQL database configuration

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/sinh57/Employee-management-system.git
cd Employee-management-system
```

### 2. Run the Backend

Navigate to the backend directory:

```bash
cd backend
```

Configure your database connection in `src/main/resources/application.properties`. Set your MySQL database URL, username, and password using your local configuration.

Start the Spring Boot application:

```bash
mvn spring-boot:run
```

The backend API will be available at:

`http://localhost:8080`

#### Using the H2 In-Memory Database

If the H2 profile is configured in the project, you can run:

```bash
mvn spring-boot:run -Dspring-boot.run.profiles=h2
```

### 3. Run the Frontend

Open a new terminal from the project root and run:

```bash
cd frontend
npm install
npm start
```

The React application will normally open at:

`http://localhost:3000`

Ensure the frontend API configuration points to the correct backend URL.

## REST API Endpoints

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/api/employees` | Retrieve all employees |
| GET | `/api/employees/{id}` | Retrieve an employee by ID |
| POST | `/api/employees` | Create an employee |
| PUT | `/api/employees/{id}` | Update an employee |
| DELETE | `/api/employees/{id}` | Delete an employee |
| GET | `/api/employees/department/{dept}` | Filter employees by department |
| GET | `/api/employees/search?name=xyz` | Search employees by name |

## Running Tests

From the backend directory, execute:

```bash
mvn test
```

This runs the backend tests configured in the project.

## Future Improvements

- Implement authentication and authorization using Spring Security and JWT
- Add pagination and sorting
- Introduce department management
- Add employee profile image uploads
- Expand automated test coverage
- Improve deployment and Docker configuration

## Learning Objectives

This project demonstrates practical use of:

- Java and object-oriented programming
- Spring Boot application development
- REST API design
- Layered architecture using controllers, services, and repositories
- Database integration with Spring Data JPA and Hibernate
- React component-based development
- Frontend-to-backend API communication
- Input validation and exception handling

---

**Note:** Configure your own database credentials and deployment settings before running the application. Never commit passwords, API keys, or other sensitive information to GitHub.
