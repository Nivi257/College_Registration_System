# College_Registration_System
A full-stack application for college registration that performs CRUD operations using Angular for the frontend, Spring Boot for the backend, and MySQL for the database.

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Usage](#usage)
- [Project Structure](#project-structure)


## Description

The College Registration System is designed to manage student information for a college. It allows users to perform Create, Read, Update, and Delete (CRUD) operations on student data. The frontend is built using Angular, providing a dynamic and responsive user interface, while the backend is built using Spring Boot, providing a robust and scalable REST API. MySQL is used as the database for persistent storage of student data.

## Features

- Add new students
- View list of students
- Update student information
- Delete students
- Responsive and user-friendly interface

## Technologies Used

- **Frontend**: Angular, HTML, CSS, Bootstrap
- **Backend**: Spring Boot, Java
- **Database**: MySQL

## Prerequisites

Before setting up the project, ensure you have the following installed on your system:

- Node.js and npm (for Angular)
- Angular CLI
- Java Development Kit (JDK) 8 or later
- Apache Maven
- MySQL

## Setup Instructions

### Backend Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/college-registration-system.git
    ```

2. Navigate to the backend directory:
    ```bash
    cd college-registration-system/backend
    ```

3. Configure the MySQL database:
    - Create a database named `college_registration` in MySQL.
    - Update the `src/main/resources/application.properties` file with your MySQL database credentials:
        ```properties
        spring.datasource.url=jdbc:mysql://localhost:3306/college_registration
        spring.datasource.username=yourusername
        spring.datasource.password=yourpassword
        spring.jpa.hibernate.ddl-auto=update
        ```

4. Build and run the Spring Boot application:
    ```bash
    ./mvnw spring-boot:run
    ```

### Frontend Setup

1. Navigate to the frontend directory:
    ```bash
    cd college-registration-system/frontend
    ```

2. Install the required dependencies:
    ```bash
    npm install
    ```

3. Run the Angular application:
    ```bash
    ng serve
    ```

4. Open your browser and navigate to `http://localhost:4200` to view the application.

## Usage

Once the frontend and backend are running, you can perform CRUD operations on student data via the web interface:

- **Add Student**: Click on "Add Student" button and fill in the form.
- **View Students**: The homepage displays a list of all students.
- **Edit Student**: Click on the "Edit" button next to a student to update their information.
- **Delete Student**: Click on the "Delete" button next to a student to remove them from the list.

## Project Structure

### Backend

- `src/main/java/com/example/college/` - Main package for Spring Boot application.
- `src/main/java/com/example/college/controller/` - REST controllers.
- `src/main/java/com/example/college/model/` - Data models.
- `src/main/java/com/example/college/repository/` - Repositories for data access.
- `src/main/java/com/example/college/service/` - Service layer for business logic.

### Frontend

- `src/app/` - Main Angular application folder.
- `src/app/components/` - Angular components.
  - `student/` - Component for displaying student list.
  - `add-student/` - Component for adding a new student.
  - `edit-student/` - Component for editing an existing student.
- `src/app/services/` - Angular services for HTTP communication with backend.
