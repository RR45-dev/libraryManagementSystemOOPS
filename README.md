# libraryManagementSystem

Library Management System - API
This is a backend API for a Library Management System built using ASP.NET Core. The system includes features for managing users and library items (books) while demonstrating key Object-Oriented Programming (OOP) principles such as Encapsulation, Inheritance, Polymorphism, Abstraction, Exceptions, Collections, and more.

Key Concepts Covered
Encapsulation: Private fields are used to restrict direct access to the data, providing controlled access via public properties.
Properties: Fields are accessed and validated through properties, which ensure proper data integrity.
Constructors: Used to initialize objects and enforce required data during object creation.
Polymorphism: Derived classes override base methods to provide customized behavior.
Abstraction: Abstract classes and methods are used to define a blueprint for derived classes.
Enums: Predefined constant values that represent specific roles (Admin/Member) and book genres.
Collections: Library items and users are managed in collections (lists).
Exception Handling: The system handles invalid inputs, missing data, and operation errors with appropriate exceptions.
File Handling: Actions like adding books or borrowing them are logged into a file.
Type Checking: The system checks the runtime type of an object to perform specific actions.
Technologies Used
ASP.NET Core 6.0
C#
Entity Framework Core (for database access)
Swagger (for API documentation and testing)
Project Structure
Models/: Contains data models such as User, Admin, Member, Book, and LibraryItem.
Services/: Contains the business logic and methods to manage users and books, such as AddBook(), AddUser(), and BorrowBook().
Controllers/: Contains the API controllers that expose endpoints for the frontend to interact with.
Features
User Management: Create, read, and manage users with Admin and Member roles.
Library Item Management: Add and manage books, with different formats such as Physical and EBooks.
Borrowing System: Members can borrow books, and Admins manage users.
Logging: Actions such as adding users and borrowing books are logged to a file.
Setup Instructions
Prerequisites
.NET 6.0 SDK or later installed on your machine.
Visual Studio 2022 or Visual Studio Code (optional, but recommended).
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/library-management-api.git
cd library-management-api
2. Restore Dependencies
Make sure to restore all NuGet packages:

bash
Copy
Edit
dotnet restore
3. Run the Application
Run the application using the following command:

bash
Copy
Edit
dotnet run
By default, the application will be hosted on https://localhost:5001.

4. Access Swagger UI
You can access Swagger for testing the API at:

bash
Copy
Edit
https://localhost:5001/swagger
5. Available Endpoints
POST /api/users/add-user: Add a new user to the system.

Request Body:
json
Copy
Edit
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "role": "Admin"
}
GET /api/users: Get a list of all users.

GET /api/users/{id}: Get details of a specific user by id.

POST /api/books/add-book: Add a new book to the library.

Request Body:
json
Copy
Edit
{
  "id": 1,
  "title": "Book Title",
  "author": "Author Name",
  "genre": "Fiction",
  "type": "PhysicalBook",
  "pages": 350
}
POST /api/borrow-book: Borrow a book by a user.

Request Body:
json
Copy
Edit
{
  "bookId": 1,
  "userId": 1
}
6. Sample Request Example
To add a new user via POST request:

json
Copy
Edit
{
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "role": "Admin"
}
7. Error Handling
The API will return 400 Bad Request if the role is invalid, or the book or user is not found.

Contributing
Feel free to fork the repository and submit pull requests if you'd like to contribute. Issues and feature requests are welcome!

License
This project is licensed under the MIT License - see the LICENSE file for details.

This README covers all aspects of your project, and it's ready to be used on GitHub! Let me know if you'd like any further modifications or additions.
