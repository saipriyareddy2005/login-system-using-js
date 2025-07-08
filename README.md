# login-system-using-js
# 🔐 JWT Authentication System – `jwt_alpha`

This is a simple and secure **User Authentication Backend** using **Node.js**, **Express**, **MongoDB**, and **JWT (JSON Web Tokens)**. The system allows users to register, log in, and access protected routes using token-based authentication.

---

## 📦 Features

- ✅ User registration with email and password
- ✅ Secure login and JWT token generation
- ✅ Passwords hashed using `bcrypt`
- ✅ Protected route (`/profile`) that requires valid JWT
- ✅ MongoDB integration using `mongoose`
- ✅ Clean code structure with MVC design pattern

---

## 🧰 Tech Stack

- **Backend**: Node.js, Express
- **Database**: MongoDB with Mongoose
- **Security**: bcrypt, jsonwebtoken
- **Environment Configuration**: dotenv

---

## 📁 Project Structure

jwt_alpha/
├── config/
│   └── db.js           # MongoDB connection setup
├── controllers/
│   └── authController.js
├── middleware/
│   └── auth.js         # JWT verification middleware
├── models/
│   └── User.js         # Mongoose user schema
├── routes/
│   └── auth.js         # Authentication routes
├── .env                # Environment variables
├── server.js           # Entry point
├── package.json


Prerequisites
Node.js & npm

MongoDB (local or MongoDB Atlas)

**Installation**
Clone the repository:

bash

git clone https://github.com/your-username/jwt_alpha.git
cd jwt_alpha

**Install dependencies:**

bash
npm install
Set up .env file in the root directory:

env

PORT=5000
MONGODB_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret_key

**Start the server:**

bash
Copy
Edit
node server.js
The server should be running at http://localhost:5000.

🧪 API Endpoints
Method	Endpoint	Description	Auth Required
POST	/api/signup	Register new user	No
POST	/api/signin	Login and get JWT token	No
GET	/api/profile	Get user profile	Yes (JWT)

🔐 How JWT Works Here
After login, a JWT token is sent back to the user.

For protected routes like /api/profile, the client must include this token in the Authorization header:

makefile

Authorization: Bearer <your_token>
