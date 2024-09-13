# Library Management System - XAMPP Setup

## Objective
This Library Management System allows users to manage books, authors, users, and borrowing records. This guide will show you how to set up and run the project using XAMPP.

## How to Run This Project on XAMPP

### Prerequisites
- XAMPP (PHP >= 7.4)
- Web browser
- Download the project zip file

### Database Configuration

1. **Open phpMyAdmin**:  
   Launch XAMPP and start the Apache and MySQL services. Then, open your browser and navigate to `http://localhost/phpmyadmin`.

2. **Create Database**:  
   In phpMyAdmin, create a new database named `library`.

3. **Import the Database**:  
   Import the provided `library.sql` file into the `library` database. The SQL file is available inside the project zip package.

### User Interface Setup

1. **Access the User Interface**:  
   Open your web browser and enter the following URL:  
   `http://localhost/library`

2. **User Login Details**:  
   - **Username**: `test@gmail.com`  
   - **Password**: `Test@123`

### Admin Panel Setup

1. **Access the Admin Panel**:  
   Open your browser and navigate to:  
   `http://localhost/library/admin`

2. **Admin Login Details**:  
   - **Username**: `admin`  
   - **Password**: `Test@123`

---

## Additional Information

### Features

- **Role-Based Access Control**: Users can either be admins, librarians, or members, with varying permissions for managing books, users, and borrow records.
- **Book and Author Management**: Admins and librarians can manage books and authors (create, update, delete).
- **Borrow/Return Books**: Members can borrow or return books, and admins can view all borrowing records.
- **User Registration and Authentication**: Supports user registration and login for all roles.
- **Search & Pagination**: Search books by title, author, or ISBN, with pagination support.

### Technical Setup for Development (Optional)

If you are a developer or want to explore the technical details further, here are the instructions for setting up the backend:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Boy2700/Backend-assessment-Yusuf-babatunde.git
   cd Backend-assessment-Yusuf-babatunde
Install dependencies:

bash
Copy code
composer install
Set up the environment: Copy .env.example to .env and configure your database credentials.

bash
Copy code
cp .env.example .env
Generate application key:

bash
Copy code
php artisan key:generate
Run migrations:

bash
Copy code
php artisan migrate
Seed the database (optional):

bash
Copy code
php artisan db:seed
Run the application:

bash
Copy code
php artisan serve
The application will be available at http://localhost:8000.

Pushing to GitHub
If you need to push this project to GitHub, use the following commands:

bash
Copy code
git remote add origin https://github.com/Boy2700/Backend-assessment-Yusuf-babatunde.git
git branch -M main
git push -u origin main
License
This project is licensed under the MIT License.

csharp
Copy code

This README file is designed for users setting up the project via XAMPP, with sections on database configuration, user/admin access, and development setup.





