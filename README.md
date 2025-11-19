# 🗺️ Natours Travel App

A travel booking web app & REST API built with Node.js, Express & MongoDB.

## 🧰 Tech Stack

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge\&logo=node.js\&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge\&logo=express\&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge\&logo=mongodb\&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=for-the-badge\&logo=mongoose\&logoColor=white)

Live demo: **[https://natours.dev](https://natours.dev)**

---

## 📌 Summary

Natours is a full-featured tour booking application and API.
It includes authentication, role-based authorization, CRUD operations, secure endpoints, and a structured MVC architecture.
Data is stored in MongoDB Atlas, and pages are rendered using Pug templates.

---

## ✨ Features

* User authentication (signup, login, password reset)
* Role-based permissions (user, guide, lead-guide, admin)
* Tours CRUD (create, read, update, delete)
* Reviews system with nested routing
* Geospatial queries (e.g., “tours within distance”)
* Secure API (rate limiting, sanitization, CORS, Helmet, HPP)
* API versioning
* Server-side rendered pages (Pug)

---

## 📂 Project Structure

```
natours/
│
├── controllers/      # Route controllers
├── models/           # Mongoose schemas
├── routes/           # API routes (v1)
├── utils/            # Helpers (APIFeatures, emails, error handling)
├── public/           # Frontend assets
├── views/            # Pug templates
│
├── app.js            # Express app definition
├── server.js         # Application entrypoint
└── config.env        # Environment variables
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/tysker/natours-travel-app.git
cd natours-travel-app
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create `config.env` in the project root:

```
NODE_ENV=development
PORT=3000

DATABASE=mongodb+srv://<USERNAME>:<PASSWORD>@cluster.mongodb.net/natours
DATABASE_PASSWORD=yourpassword

JWT_SECRET=yourjwtsecret
JWT_EXPIRES_IN=90d

EMAIL_HOST=smtp.example.com
EMAIL_USERNAME=yourEmailUsername
EMAIL_PASSWORD=yourEmailPassword
```

Adjust according to your version.

### 4. Start development server

```bash
npm run start:dev
```

Runs at:

```
http://localhost:3000
```

---

## 📡 API Overview

Base URL:

```
https://natours.dev/api/v1
```

### Example Endpoints

* `GET /tours` – list all tours
* `GET /tours/:id` – get a specific tour
* `POST /users/signup` – create a new user
* `POST /users/login` – login
* `PATCH /users/updateMe` – update current user
* `GET /tours-within/:distance/center/:latlng/unit/:unit` – geospatial query

If you want, we can add a standalone **API.md**.

---

## 🧠 Why This Project Exists

This project demonstrates modern backend architecture for the Node.js ecosystem:

* MVC pattern
* Secure production-ready REST API
* Real database modeling with Mongoose
* Middleware workflows
* Authentication/authorization
* Error handling patterns
* Environment-based configuration
