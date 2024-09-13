How to run this Library Management System Project on Xampp


Database Configuration

Open phpmyadmin
Create Database�library
Import database library.sql (available inside zip package)

For User

Open Your browser put inside browser �http://localhost/library�
Login Details for user:�
Username: test@gmail.com
Password: Test@123

For Admin Panel

Open Your browser put inside browser �http://localhost/library/admin�
Login Details for admin :�
Username: admin
Password:Test@123




Here's the complete README.md file content with the setup instructions you can directly copy and paste into your repository. It includes the markdown formatting:

```markdown
# Library Management System - Backend Technical Assessment

## Objective
The purpose of this project is to build a RESTful API for a library management system. The API will allow for managing books, authors, users, and borrow records. Additionally, it incorporates role-based access control (RBAC), search capabilities, and caching. The project is built using **Laravel** and utilizes a relational database, such as **MySQL**.

## Features
1. **Role-Based Access Control (RBAC)**:  
   - Admin: Full access to all resources.  
   - Librarian: Manage books and authors, view borrow records, but no user management.  
   - Member: Can borrow/return books, view books and authors, and update profile.

2. **Book Management**:  
   Create, update, delete, and retrieve books with information about the author, availability, and status (Available/Borrowed).

3. **Author Management**:  
   Create, update, delete, and retrieve information about authors.

4. **User Management**:  
   Registration, authentication, and role management for users (Admin, Librarian, Member).

5. **Borrow and Return System**:  
   Track borrowing and returning books with due dates, allowing members to manage their book loans.

6. **Search**:  
   Implement search functionality for books by title, author, or ISBN.

7. **Pagination**:  
   Pagination support for listing books, authors, and borrow records.

8. **Input Validation**:  
   Ensure all inputs are properly validated before processing requests.

9. **Error Handling**:  
   Implement error handling with proper HTTP status codes and descriptive messages.

10. **Testing**:  
    Unit and feature tests to ensure functionality is properly tested.

11. **Bonus Features**:
    - **Rate Limiting**: Prevent abuse by limiting API requests.
    - **Docker Support**: Containerized deployment using Docker.

## API Endpoints

### Books
- **GET** `/books`: Retrieve a list of all books.
- **GET** `/books/{id}`: Retrieve details of a specific book by ID.
- **POST** `/books`: Create a new book (Admin/Librarian only).
- **PUT** `/books/{id}`: Update an existing book by ID (Admin/Librarian only).
- **DELETE** `/books/{id}`: Delete a book by ID (Admin only).
- **POST** `/books/{id}/borrow`: Borrow a book (Member only, if available).
- **POST** `/books/{id}/return`: Return a borrowed book (Member only).

### Authors
- **GET** `/authors`: Retrieve a list of all authors.
- **GET** `/authors/{id}`: Retrieve details of a specific author by ID.
- **POST** `/authors`: Create a new author (Admin/Librarian only).
- **PUT** `/authors/{id}`: Update an existing author by ID (Admin/Librarian only).
- **DELETE** `/authors/{id}`: Delete an author by ID (Admin only).

### Users
- **GET** `/users`: Retrieve a list of all users (Admin only).
- **GET** `/users/{id}`: Retrieve details of a specific user by ID (Admin only).
- **POST** `/users`: Register a new user.
- **PUT** `/users/{id}`: Update user details (Admin only or self).
- **DELETE** `/users/{id}`: Delete a user by ID (Admin only).
- **POST** `/login`: Authenticate a user and return a Sanctum token.

### Borrow Records
- **GET** `/borrow-records`: Retrieve all borrow records (Admin/Librarian only).
- **GET** `/borrow-records/{id}`: Retrieve details of a specific borrow record by ID (Admin/Librarian only).

## Setup Instructions

### Prerequisites
- PHP >= 8.0
- Composer
- MySQL/PostgreSQL/SQLite
- Laravel
- Docker (optional)

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Boy2700/Backend-assessment-Yusuf-babatunde.git
   cd Backend-assessment-Yusuf-babatunde
   ```

2. **Install dependencies**:
   ```bash
   composer install
   ```

3. **Set up the environment**:
   Copy the `.env.example` to `.env` and configure your database credentials.
   ```bash
   cp .env.example .env
   ```

4. **Generate application key**:
   ```bash
   php artisan key:generate
   ```

5. **Run migrations**:
   ```bash
   php artisan migrate
   ```

6. **Seed the database** (optional):
   You can seed the database with sample data using:
   ```bash
   php artisan db:seed
   ```

7. **Run the application**:
   Start the local development server:
   ```bash
   php artisan serve
   ```

8. **Access the API**:
   The API will be available at `http://localhost:8000`.

### Running Tests
To run the feature and unit tests, execute the following command:
```bash
php artisan test
```

### Docker Setup (Optional)
To use Docker for easier deployment, follow these steps:
1. Ensure Docker is installed.
2. Build and run the application using Docker:
   ```bash
   docker-compose up --build
   ```

The application will be available at `http://localhost:8000`.

## Documentation
You can use Postman or Swagger to document and test the API endpoints.

## License
This project is licensed under the MIT License.

## Pushing to GitHub
To push your project to GitHub, follow these steps:

```bash
git remote add origin https://github.com/Boy2700/Backend-assessment-Yusuf-babatunde.git
git branch -M main
git push -u origin main
```
```
