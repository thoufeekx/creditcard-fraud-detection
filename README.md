Here’s an updated **README.md** with the introductory section included, followed by the current status:

---

# Fraud Detection System

## Project Overview

This project is a comprehensive **Fraud Detection System** aimed at monitoring and managing financial transactions. It is being developed as part of the **Winter Semester 2025 project** with a focus on building a robust, scalable, and secure application.

### **Objectives**
- Build a transaction monitoring system with both user-facing components and backend logic.
- Implement real-time visualizations and REST APIs for transaction data retrieval.
- Develop microservices for user authentication, transaction processing, and reporting.
- Enable live AI-based predictions to detect fraudulent transactions and provide proactive alerts.
- Ensure scalability, security, and reliability through containerization, orchestration, and monitoring.

### **Technologies**
- **Frontend**: Vue.js, JavaScript.
- **Backend**: FastAPI (Python), SQLAlchemy ORM.
- **Database**: MySQL for transaction logs, user profiles, and analytics data.
- **Containerization**: Docker, Docker Compose.
- **Future Plans**: Kubernetes (AKS), CI/CD pipelines, and AI/ML integration for fraud detection.

### **Backend Features**
- **Admin-Specific Features**:
  - Transaction approvals.
  - User role management.
- **Authentication**:
  - Stateless JWT-based authentication.
  - Role-Based Access Control (RBAC) with admin and user roles.
- **Endpoints**:
  - `/register`, `/login`, `/logout` for user management.
  - `/transactions` for managing transactions.
  - `/reports` for generating reports.

---

## Current Status

### 1. **Database Integration**
- The backend is successfully connected to a MySQL database (`FraudDetection`).
- Current tables:
  - **`users`**: Stores credit card user data.
  - **`transactions`**: Stores transaction records.

### 2. **Backend Functionality**
- API built with **FastAPI**.
- Current endpoints:
  - `GET /`: Root endpoint to verify API is running.
  - `GET /users`: Fetch all users from the `users` table.
  - `GET /users/{user_id}`: Fetch a specific user by their `user_id`.

### 3. **Testing**
- Verified API functionality through Swagger UI at `http://localhost:8000/docs`.
- User data successfully fetched from the database.

---

## Next Steps

### 1. **Admin Features**
- Create an `admins` table and migrate it to the database using Alembic.
- Implement Role-Based Access Control (RBAC) for admin-only endpoints.

### 2. **Secure Endpoints**
- Use JWT tokens to secure all endpoints.
- Restrict access to admin-specific routes.

### 3. **Testing**
- Test the RBAC implementation with both admin and user roles.
- Ensure proper error handling and validation.

---

## How to Run the Project

### **Prerequisites**
- Docker and Docker Compose installed.
- Python dependencies listed in `requirements.txt`.

### **Steps**
1. **Build and Start Services:**
   ```bash
   docker compose up --build -d
   ```
2. **Access API Documentation:**
   Open `http://localhost:8000/docs` in your browser.

3. **Database Access:**
   Connect to MySQL at `localhost:3306` using a database client.

---
