<div align="center">
🗺️ Natours Travel App

A travel booking web app & REST API built with Node.js, Express & MongoDB.

<br/> <!-- Tech Logos --> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js" width="80" height="80"/> &nbsp;&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original.svg" alt="Express" width="80" height="80"/> &nbsp;&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="MongoDB" width="80" height="80"/> &nbsp;&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongoose/mongoose-original.svg" alt="Mongoose" width="80" height="80"/>

<br/><br/>

Live demo: https://natours.dev

--- 

# 🗺️ Natours Travel App

A travel booking web app & REST API built with **Node.js**, **Express**, and **MongoDB (Mongoose)**.
Live demo: **[https://natours.dev](https://natours.dev)**

---

## 📌 Summary

This project is a full-featured tour booking application built during a course. It includes authentication, authorization, user & tour management, secure API endpoints, and a clean MVC architecture. Data is stored in MongoDB Atlas. The frontend uses server-side rendering with Pug templates.

---

## ✨ Features

* User authentication (sign up, login, password reset)
* Role-based authorization (user, guide, admin)
* Tours CRUD (create, read, update, delete)
* Reviews system with nested routes
* Geospatial queries (e.g., "tours within distance")
* Payment flow (Stripe) – if included in your version
* Server-side rendered pages (Pug templates)
* Security best practices:

  * Rate limiting
  * Sanitization
  * CORS
  * Helmet
  * HPP
* API versioning

---

## 🛠️ Tech Stack

**Backend / API**

* Node.js
* Express
* MongoDB Atlas
* Mongoose ORM

**Frontend**

* Pug template engine
* Tailwind / custom CSS (if applicable)

**Dev Tools**

* nodemon
* eslint
* Prettier

---

## 📂 Project Structure

```
natours/
│
├── controllers/      # Route controllers for tours, users, reviews, bookings
├── models/           # Mongoose models
├── routes/           # API routes (v1)
├── utils/            # Helpers (API features, email, error handling)
├── public/           # Frontend assets (JS, images, CSS)
├── views/            # Pug templates for the website
│
├── app.js            # Express app setup
├── server.js         # App entrypoint
└── config.env        # Environment variables
```

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/tysker/natours-travel-app.git
cd natours-travel-app
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

Create a file named `config.env` in the project root:

```
NODE_ENV=development
PORT=3000

DATABASE=mongodb+srv://<USERNAME>:<PASSWORD>@cluster.mongodb.net/natours
DATABASE_PASSWORD=yourpassword

JWT_SECRET=yourjwtsecret
JWT_EXPIRES_IN=90d

EMAIL_USERNAME=...
EMAIL_PASSWORD=...
EMAIL_HOST=...
```

(Include only what your version actually uses.)

### 4. Start the development server

```bash
npm run start:dev
```

The app runs at:
`http://localhost:3000`

---

## 📡 API Overview

### Base URL

```
https://natours.dev/api/v1
```

### Example Endpoints

* **GET /tours** — list all tours
* **GET /tours/:id** — get one tour
* **POST /tours** — create new tour (admin only)
* **POST /users/signup** — register new user
* **POST /users/login** — login
* **PATCH /users/updateMe** — update logged-in user
* **GET /tours-within/:distance/center/:latlng/unit/:unit** — geospatial query

Add a link to `api-docs.md` if you create one.

---

## 🧠 Why This Project Exists

This project was built as part of learning modern Node.js backend development, focusing on real-world architecture:

* MVC design pattern
* Secure production-ready REST API
* Database modeling & data relationships
* Middleware patterns
* Error handling best practices
* Environment-based config

Just say the word and we can expand it.
