# Book Management System

This project is a simple CRUD (Create, Read, Update, Delete) application for managing a collection of books. It is built with **Spring Boot**, uses **JPA/Hibernate** for database interaction, and has a simple frontend built with **HTML, CSS, and JavaScript**.

----------

## Features

-   **Add a new book**: You can add a new book with a title, author, price, and an optional image URL.

-   **View all books**: All the books in the database are displayed on the main page.

-   **Update a book**: You can edit the details of an existing book.

-   **Delete a book**: You can remove a book from the database.

-   **View full-size book cover image**: Clicking on a book's cover image will display a larger version.


----------

## Technologies Used

### Backend

-   **Spring Boot**: A framework that makes it easy to create stand-alone, production-grade Spring-based Applications that you can "just run".

-   **Spring Data JPA**: Part of the larger Spring Data family, it makes it easy to easily implement JPA based repositories.

-   **Hibernate**: A popular implementation of the Java Persistence API (JPA) specification.

-   **MySQL Connector/J**: The official JDBC driver for MySQL.

-   **java-dotenv**: A library to load environment variables from a `.env` file.


### Frontend

-   **HTML**: The standard markup language for creating web pages.

-   **CSS**: A style sheet language used for describing the presentation of a document written in a markup language like HTML.

-   **JavaScript**: A programming language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else.


----------

## Setup and Installation

1.  **Clone the repository**:

    Bash

    ```
    git clone https://github.com/rahmasir/crud-rest-jpa-demo.git
    ```

2.  **Create a `.env` file**: In the root of the project, create a file named `.env` and add the following, replacing the placeholder values with your MySQL database credentials. You can refer to the provided `.env.example` file.

    ```
    DB_URL=jdbc:mysql://localhost:3306/your_database_name
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    ```

3.  **Run the application**: You can run the application using your IDE or by using the Maven wrapper.

    Bash

    ```
    ./mvnw spring-boot:run
    ```


The application will be accessible at `http://localhost:8080`.

----------

## API Endpoints

The `BookController.java` class defines the following RESTful endpoints for managing books.

-   `POST /books`: Creates a new book.

-   `GET /books`: Retrieves a list of all books.

-   `PUT /books/{id}`: Updates an existing book.

-   `DELETE /books/{id}`: Deletes a book.


----------

## How It Works

The application follows a standard layered architecture:

-   **`Book.java`**: This is the entity class that represents a book in the database.

-   **`BookRepository.java`**: This is a JPA repository interface that provides methods for CRUD operations and some custom queries.

-   **`BookController.java`**: This is a REST controller that exposes the API endpoints for interacting with the book data.

-   **`index.html`**: This is the main page of the application, which includes a form for adding books and a grid to display them. It uses JavaScript to make asynchronous API calls to the backend to perform CRUD operations.