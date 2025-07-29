
# 📚 ReadHub – Library System (Backend)

**ReadHub** is a full-featured backend system designed to manage library operations efficiently. Built using **Node.js**, **Express**, **TypeScript**, and **MongoDB**, this backend provides secure APIs to handle books, readers, lendings, user authentication, and automated overdue notifications.

---

## 🚀 Core Features

- 🔐 **JWT Authentication & Authorization**
- 📘 **Book Management API** (CRUD)
- 👥 **Reader Management API** (CRUD)
- 📅 **Lending System API** (Issue, Return, Overdue Handling)
- 📬 **Email Reminders** for Overdue Books (SendGrid)
- 📊 **Admin Dashboard Data API**
- 📦 **Modular Folder Structure with Middleware & Validation**

---

## 🛠️ Tech Stack

| Layer         | Technology                  |
|---------------|------------------------------|
| Runtime       | Node.js                      |
| Framework     | Express.js                   |
| Language      | TypeScript                   |
| Database      | MongoDB + Mongoose           |
| Auth          | JWT (JSON Web Tokens)        |
| Email         | SendGrid (Email API)         |
| Others        | dotenv, cors, express-validator, bcrypt

---

## 📦 Getting Started

### 1. Clone the Repository

```bash
https://github.com/AchiniPramo/ReadHub_Online_Library_System_Backend-.git

````

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Configuration

Create a `.env` file in the root directory and add the following:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
SENDGRID_API_KEY=your_sendgrid_api_key
FROM_EMAIL=your_verified_sendgrid_email
```

> ✅ Make sure your SendGrid account is verified and email sending is enabled.

### 4. Run the Development Server

```bash
npm run dev
```

Server will run at `http://localhost:3000`

---

## 📁 Folder Structure

```
src/
├── controllers/       # Request handlers (books, readers, lendings, auth)
├── routes/            # API route definitions
├── models/            # Mongoose models
├── middleware/        # JWT auth, error handlers
├── utils/             # Token & email utilities
├── config/            # DB and email config
└── index.ts           # App entry point
```

---

## 🔐 Authentication & Security

* Passwords hashed with **bcrypt**
* JWT tokens stored in HTTP headers
* Access restricted by **user roles**
* Routes protected using middleware

---

## 📬 Email Notifications

Uses **SendGrid** to send overdue reminders:

* Scheduled via CRON or manual triggers
* Email content customizable in the utility

---

## 📡 API Endpoints Overview

| Resource  | Routes (examples)                          |
| --------- | ------------------------------------------ |
| Auth      | `POST /api/auth/login`, `GET /api/auth/me` |
| Books     | `GET /api/books`, `POST /api/books`        |
| Readers   | `GET /api/readers`, `PUT /api/readers/:id` |
| Lending   | `POST /api/lend`, `PATCH /api/return/:id`  |
| Dashboard | `GET /api/dashboard/overview`              |

> Full API documentation can be added with Swagger or Postman collection.

---
