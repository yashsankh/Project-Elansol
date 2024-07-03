# Full Stack Login and Registration System

## Project Overview

This project is a simple login and registration system developed using React for the front end and Node.js with MongoDB for the back end. The application includes:
- A registration form where users can sign up by providing their name, date of birth, email, and password.
- A login form where registered users can log in using their email and password.
- Protected routes to ensure that only logged-in users can access certain pages.
- User information stored in the browser's local storage after successful login or registration.
- A static table displayed on the protected page.

## Tech Stack

### Frontend
- React
- React-Bootstrap
- Axios
- React Router

### Backend
- Node.js
- Express
- MongoDB
- Mongoose
- bcryptjs
- jsonwebtoken
- cors
- dotenv

## Project Structure

full-stack-app/
├── backend/
│ ├── config/
│ │ └── db.js
│ ├── controllers/
│ │ └── authController.js
│ ├── middleware/
│ │ └── authMiddleware.js
│ ├── models/
│ │ └── User.js
│ ├── routes/
│ │ └── authRoutes.js
│ ├── .env
│ ├── package.json
│ └── server.js
└── frontend/
├── public/
├── src/
│ ├── components/
│ │ ├── LoginForm.js
│ │ ├── RegisterForm.js
│ │ ├── Dashboard.js
│ │ └── ProtectedRoute.js
│ ├── App.js
│ ├── index.js
│ ├── api.js
│ ├── auth.js
│ └── styles.css
├── package.json
└── README.md


## Backend Setup

1. Navigate to the backend directory:
    ```bash
    cd backend
    ```

2. Install the required dependencies:
    ```bash
    npm install
    ```

3. Create a `.env` file and add your MongoDB connection string and JWT secret:
    ```env
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret
    ```

4. Create the necessary files:
    - `server.js`: Entry point for the backend server.
    - `config/db.js`: MongoDB connection configuration.
    - `controllers/authController.js`: Authentication logic.
    - `middleware/authMiddleware.js`: Middleware to protect routes.
    - `models/User.js`: User model schema.
    - `routes/authRoutes.js`: Authentication routes.

5. Start the backend server:
    ```bash
    npm run dev
    ```

## Frontend Setup

1. Navigate to the frontend directory:
    ```bash
    cd ../frontend
    ```

2. Install the required dependencies:
    ```bash
    npm install
    ```

3. Create the necessary files:
    - `src/components/LoginForm.js`: Login form component.
    - `src/components/RegisterForm.js`: Registration form component.
    - `src/components/Dashboard.js`: Protected dashboard component.
    - `src/components/ProtectedRoute.js`: Higher-order component for protected routes.
    - `src/App.js`: Main application component.
    - `src/index.js`: Entry point for the React application.
    - `src/api.js`: Axios instance for API calls.
    - `src/auth.js`: Utility functions for authentication.
    - `src/styles.css`: Custom styles.

4. Start the frontend development server:
    ```bash
    npm start
    ```

## API Endpoints

### Registration
- **URL**: `/api/register`
- **Method**: `POST`
- **Body**:
    ```json
    {
        "name": "John Doe",
        "dob": "1990-01-01",
        "email": "john.doe@example.com",
        "password": "yourpassword"
    }
    ```

### Login
- **URL**: `/api/login`
- **Method**: `POST`
- **Body**:
    ```json
    {
        "email": "john.doe@example.com",
        "password": "yourpassword"
    }
    ```

## Features

- User registration and login forms.
- User authentication using JWT.
- Protected routes that require login.
- User information stored in local storage.
- Responsive design using React-Bootstrap.

