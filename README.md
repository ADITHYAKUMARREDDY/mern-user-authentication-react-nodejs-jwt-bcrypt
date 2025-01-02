# MERN Authentication Backend with JWT and Bcrypt

This project provides the backend functionality for a user authentication system using **Node.js**, **Express**, **MongoDB**, **JWT**, and **Bcrypt**. It includes user registration, login, and JWT-based authentication.

---

## Features

- **User Registration**: Hashes passwords before storing them in the database.
- **User Login**: Validates user credentials and provides a JWT token.
- **JWT Authentication**: Protects routes with JSON Web Tokens.
- **Password Hashing**: Uses Bcrypt for secure password handling.
- **Error Handling**: Custom error responses for better API feedback.

---

## Installation

### Prerequisites

- [Node.js](https://nodejs.org)
- [MongoDB](https://www.mongodb.com) (local or MongoDB Atlas instance)

### Steps

1. Clone the Repository:
   ```bash
   git clone https://github.com/ADITHYAKUMARREDDY/mern-authentication-backend-jwt-bcrypt.git
   cd mern-authentication-backend-jwt-bcrypt

npm install

Set Up Environment Variables:

Create a .env file in the root directory and add the following:
env
Copy code
PORT=5000
MONGO_URI=your-mongodb-connection-string
JWT_SECRET=your-secret-key
JWT_EXPIRES_IN=90d

Running the Application
Start the Server:

bash
Copy code
npm start
The server will run on http://localhost:5000.

API Endpoints
Register User
Endpoint: POST /api/auth/signup

Headers:

plaintext
Copy code
Content-Type: application/json
Body:

json
Copy code
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123",
  "role": "user"
}
Response:

json
Copy code
{
  "status": "success",
  "message": "User registered successfully",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2Nzc2YjcyYTQ0ZDk2NjljNWRmYTRjZTYiLCJpYXQiOjE3MzU4MzMzODYsImV4cCI6MTc0MzYwOTM4Nn0.oE_lpu7rGk06dvAWVUCrKZxnGbUYdOMSCncdlQlhJnw"
}
Login User
Endpoint: POST /api/auth/login

Headers:

plaintext
Copy code
Content-Type: application/json
Body:

json
Copy code
{
  "email": "john@example.com",
  "password": "password123"
}
Response:

json
Copy code
{
  "status": "success",
  "message": "User logged in successfully",
  "user": {
      "_id": "6776b72a44d9669c5dfa4ce6",
      "name": "John Doe",
      "email": "john@example.com",
      "role": "user"
  },
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2Nzc2YjcyYTQ0ZDk2NjljNWRmYTRjZTYiLCJpYXQiOjE3MzU4MzM1NzAsImV4cCI6MTc0MzYwOTU3MH0.2akgu5RR39-Mq-W_TCMqec9RTHbbb9od4nwoQeAPMrU"
}


Technologies Used
Backend: Node.js, Express.js
Database: MongoDB, Mongoose
Authentication: JWT (JSON Web Tokens)
Password Hashing: Bcrypt



