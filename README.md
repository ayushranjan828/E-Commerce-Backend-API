# 🛒 E-Commerce Backend API

This is a backend REST API built using **Java Spring Boot**, **Spring Data JPA**, and **MySQL** for an e-commerce application. It supports basic product CRUD (Create, Read, Update, Delete) operations and follows a layered architecture (Controller → Service → Repository → Database).

---

## 🚀 Features

- ✅ Create, read, update, and delete products
- ✅ MySQL database integration
- ✅ Clean and scalable project structure
- ✅ Built using Spring Boot best practices

---

## 🧰 Tech Stack

- **Java 17+**: The core programming language.
- **Spring Boot**: Framework for building production-ready Spring applications.
- **Spring Web**: Module for building web applications, including RESTful APIs.
- **Spring Data JPA**: Simplifies data access and persistence with JPA.
- **MySQL**: Relational database for storing product information.
- **Lombok**: Reduces boilerplate code (e.g., getters, setters, constructors).
- **Maven**: Dependency management and build automation tool.

---

## 📁 Project Structure
      It looks like you've provided the content of a README.md file for an e-commerce backend API, along with a revised version from ChatGPT.

I can help you arrange this content into a well-formatted README.md file. The ChatGPT version is already quite good, but I'll make sure it's clean, properly formatted, and includes some minor enhancements for clarity and completeness, based on best practices for README files.

Here's the properly arranged and formatted README.md content:

Markdown

# 🛒 E-Commerce Backend API

This is a backend REST API built using **Java Spring Boot**, **Spring Data JPA**, and **MySQL** for an e-commerce application. It supports basic product CRUD (Create, Read, Update, Delete) operations and follows a layered architecture (Controller → Service → Repository → Database).

---

## 🚀 Features

- ✅ Create, read, update, and delete products
- ✅ MySQL database integration
- ✅ Clean and scalable project structure
- ✅ Built using Spring Boot best practices

---

## 🧰 Tech Stack

- **Java 17+**: The core programming language.
- **Spring Boot**: Framework for building production-ready Spring applications.
- **Spring Web**: Module for building web applications, including RESTful APIs.
- **Spring Data JPA**: Simplifies data access and persistence with JPA.
- **MySQL**: Relational database for storing product information.
- **Lombok**: Reduces boilerplate code (e.g., getters, setters, constructors).
- **Maven**: Dependency management and build automation tool.

---

## 📁 Project Structure

ecommerce-backend/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/yourcompany/ecommerce/ # Replace with your package structure
│   │   │       ├── controller/ # REST API Controllers
│   │   │       ├── service/ # Business logic
│   │   │       │   └── impl/ # Service implementations
│   │   │       ├── model/ # JPA Entities (e.g., Product.java)
│   │   │       └── repository/ # JPA Repositories (e.g., ProductRepository.java)
│   │   └── resources/
│   │       └── application.properties # Database configuration and other properties
│   └── test/ # For unit and integration tests
└── pom.xml # Maven project object model

---

## ⚙️ Getting Started

### 🧱 Prerequisites

Before you begin, ensure you have the following installed:

-   **Java 17 or higher**: [Download Java](https://www.oracle.com/java/technologies/downloads/)
-   **Maven**: [Install Maven](https://maven.apache.org/install.html)
-   **MySQL Server**: [Download MySQL](https://dev.mysql.com/downloads/mysql/)

---

### 🛠️ Setup Instructions

1.  **Clone the Repository**

    ```bash
    git clone [https://github.com/yourusername/ecommerce-backend.git](https://github.com/yourusername/ecommerce-backend.git)
    cd ecommerce-backend
    ```
    *Replace `yourusername` with your actual GitHub username.*

2.  **Create MySQL Database**

    Open your MySQL client (e.g., MySQL Workbench, command line) and execute the following SQL command to create the database:

    ```sql
    CREATE DATABASE ecommerce_db;
    ```

3.  **Configure `application.properties`**

    Navigate to `src/main/resources/application.properties` and update the database connection details:

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db?useSSL=false&serverTimezone=UTC
    spring.datasource.username=root
    spring.datasource.password=your_password
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
    ```
    *Replace `your_password` with your MySQL root password.*
    *The `?useSSL=false&serverTimezone=UTC` parameters are good practice for MySQL connections.*

4.  **Run the Application**

    From the project root directory, run the Spring Boot application using Maven:

    ```bash
    mvn spring-boot:run
    ```
    The application will start on `http://localhost:8080`.

---

## 📡 API Endpoints

The API provides the following endpoints for product management:

| Method | Endpoint              | Description              |
| :----- | :-------------------- | :----------------------- |
| `POST` | `/api/products`       | Create a new product     |
| `GET`  | `/api/products`       | Get all products         |
| `GET`  | `/api/products/{id}`  | Get product by ID        |
| `DELETE` | `/api/products/{id}`  | Delete product by ID     |

### 📦 Sample Product JSON

Here's an example of a product object in JSON format:

```json
{
  "name": "Wireless Mouse",
  "description": "2.4GHz Ergonomic Mouse",
  "price": 599.0,
  "stock": 50
}


📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

⭐ Show Your Support
If you found this project helpful, please give it a ⭐ on GitHub and consider forking it!
