
# Expense Tracker API

The Expense Tracker API is a RESTful API that allows users to track their expenses. Users can perform CRUD operations on expenses and generate expense reports for a specific date range or month. Users are required to sign in or register to access the expense tracking features.

## Table of Contents
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [Authentication](#authentication)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Technologies Used

- Java 11
- Spring Boot 
- Spring Data JPA
- MySQL
- Maven

## Getting Started

1. Clone the repository:

2. Create a MySQL database and update the application properties with the database credentials.

3. Build the project:

git bash
Copy code
cd expense-tracker-api
mvn clean install
Run the application:
bash
Copy code
mvn spring-boot:run
The application will start, and the API will be accessible at http://(publicipofaws):8080/api.

API Endpoints
Authentication
POST /api/users/register: Register a new user. (Requires username and password in the request body).
POST /api/users/login: Log in an existing user. (Requires username and password in the request body).
Expenses
POST /api/expenses: Create a new expense. (Requires title, description, price, date, and userId in the request body).
GET /api/expenses: Get all expenses for a specific user.
GET /api/expenses/{expenseId}: Get details of a specific expense by its ID.
PUT /api/expenses/{expenseId}: Update an existing expense by its ID. (Requires title, description, price, date, and userId in the request body).
DELETE /api/expenses/{expenseId}: Delete an existing expense by its ID.
Reports
GET /api/expenses/date: Get all expenses for a specific date. (Requires date as a query parameter in YYYY-MM-DD format).
GET /api/expenses/report: Get the total expenditure for a user within a specified date range. (Requires From, To, and userId as query parameters in YYYY-MM-DD format).
Usage
You can use tools like Postman or cURL to interact with the API. Make sure to set the appropriate headers and request bodies when necessary.

Contributing
Contributions to the Expense Tracker API are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.