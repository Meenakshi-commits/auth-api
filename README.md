# User Authentication and Authorization with JWT

This is a **Node.js** and **Express.js** application that implements user authentication and authorization using **JWT (JSON Web Token)**. It follows the **MVC pattern** and includes API endpoints for user registration, login, and protected routes.

---

## Features
✅ User Registration (with password hashing)  
✅ User Login (JWT Token Generation)  
✅ Protected Routes (JWT Token Verification)  
✅ Error Handling & Input Validation  
✅ API Documentation in Postman  
✅ Secure Environment Variables  

---

## Tech Stack
- **Node.js**  
- **Express.js**  
- **MongoDB & Mongoose**  
- **JWT (jsonwebtoken)**  
- **dotenv** (for environment variables)  
- **Postman** (for API testing)  

---

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies
```sh
npm install
```

### 3. Set Up Environment Variables
Create a `.env` file in the root directory and add:  
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

### 4. Start the Server
```sh
npm run dev  # For development (with nodemon)
or
node server.js  # For production
```

---

## API Endpoints

### 1. Register a User
**POST** `/api/auth/register`
- **Request Body (JSON)**  
  ```json
  {
    "username": "testuser",
    "email": "test@example.com",
    "password": "password123"
  }
  ```
- **Response (Success)**  
  ```json
  {
    "message": "User registered successfully"
  }
  ```

---

### 2. Login User
**POST** `/api/auth/login`
- **Request Body (JSON)**  
  ```json
  {
    "email": "test@example.com",
    "password": "password123"
  }
  ```
- **Response (Success)**  
  ```json
  {
    "message": "Login successful",
    "token": "your_generated_jwt_token"
  }
  ```

---

### 3. Get User Data (Protected Route)
**GET** `/api/auth/user`
- **Headers**:  
  ```
  Authorization: Bearer your_generated_jwt_token
  ```
- **Response (Success)**  
  ```json
  {
    "_id": "65d0f0f6a123b456789abcd0",
    "username": "testuser",
    "email": "test@example.com"
  }
  ```

---

## Deployment
### 1. Deploy Backend to Render
1. Push your code to GitHub  
2. Go to **Render (https://render.com/)**  
3. Create a new **Web Service**  
4. Connect your **GitHub repository**  
5. Set environment variables in Render  
6. Deploy the service  


