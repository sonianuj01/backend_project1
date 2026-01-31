# YouTube Backend API

A RESTful backend service for a YouTube-like application built using the **MEN stack (MongoDB, Express.js, Node.js)** with **JWT-based authentication**.  
This project focuses on scalable backend architecture, secure authentication, and clean API design.

---

## 🚀 Features

- User registration & login
- JWT-based authentication & authorization
- Secure password hashing using bcrypt
- Video CRUD operations
- Like / dislike videos
- Comment system
- Channel subscription system
- Protected routes using middleware
- RESTful API design

---

## 🛠 Tech Stack

- **Runtime:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB (Mongoose)
- **Authentication:** JSON Web Token (JWT)
- **Security:** bcrypt, dotenv
- **API Testing:** Postman

---

## 📂 Project Structure

├── public/
│ └── temp/ # Temporary public files
├── src/
│ ├── controllers/ # Request handlers / business logic
│ ├── db/ # Database connection setup
│ ├── middlewares/ # Auth & error handling middlewares
│ ├── models/ # Mongoose schemas
│ ├── routes/ # API route definitions
│ ├── utils/ # Helper & utility functions
│ ├── app.js # Express app configuration
│ ├── constants.js # App-wide constants
│ └── index.js # Application entry point
├── .env.sample 
├── .gitignore
├── .prettierrc
├── .prettierignore
├── package.json
├── package-lock.json
└── Readme.md
