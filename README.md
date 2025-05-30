# JavaServlet-Login-Page

## Overview

This project is a simple and secure web-based Login and Registration system developed using Java technologies. It uses **JSP (JavaServer Pages)** and **Servlets** for the web layer, **JDBC** for database connectivity, and **MySQL** as the backend database.

The system enables users to register and log in with proper input validation and secure credential handling. This serves as a foundational example of implementing authentication and user session management in Java EE web applications.

---

## Features

- User Registration with form validation
- User Login with authentication
- Password match and verification
- MySQL database integration using JDBC
- Error handling and feedback messages
- Session management
- Logout functionality

---

## Technologies Used

- Java
- JSP (JavaServer Pages)
- Servlet
- JDBC (Java Database Connectivity)
- MySQL
- Apache Tomcat (or any other Java EE server)

---

## Setup Instructions

### Prerequisites

- JDK 8 or above
- Apache Tomcat 9 or above
- MySQL Server
- MySQL Workbench or any SQL client
- IDE (Eclipse, IntelliJ IDEA, or NetBeans)

### Database Setup

1. Create a database named `userdb` in MySQL.
2. Run the following SQL script to create the users table:

```sql
CREATE DATABASE IF NOT EXISTS userdb;

USE userdb;

CREATE TABLE users (
    id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    password VARCHAR(100),
    PRIMARY KEY (id)
);
```

### Configuration

1. Update database connection details in `DBConnection.java` (URL, username, password).
2. Deploy the project on Apache Tomcat.
3. Access the application via `http://localhost:8080/JavaServlet-Login-Page`

---

## Folder Structure

```
JavaServlet-Login-Page/
├── src/
│   ├── com.login/
│   │   ├── LoginServlet.java
│   │   ├── RegisterServlet.java
│   │   └── DBConnection.java
├── WebContent/
│   ├── login.jsp
│   ├── register.jsp
│   ├── home.jsp
│   └── logout.jsp
├── web.xml
```

---

## Author

This project was developed as part of a learning initiative to understand Java-based web application development using Servlets and JSP.

---

## License

This project is open-source and available for educational and non-commercial use.
