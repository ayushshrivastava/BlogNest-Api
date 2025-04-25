# 🪶 BlogNest API

**BlogNest API** is a secure and scalable backend API for a blogging platform. Built using **Node.js**, **Express.js**, and **MongoDB**, this project includes user authentication, post management, and secure route handling with tools like **JWT**, **bcryptjs**, and **Helmet**.

---

## 🧰 Tech Stack

- **Backend:** Node.js, Express.js  
- **Database:** MongoDB with Mongoose  
- **Authentication:** JWT & bcryptjs  
- **Validation:** Joi  
- **Security:** Helmet, Cookie-Parser, CORS  
- **Email Services:** Nodemailer  
- **Other:** dotenv, nodemon (for development)

---


## 🏃 Scripts

| Command         | Description                   |
|----------------|-------------------------------|
| `npm start`     | Run in production mode        |
| `npm run dev`   | Run in development (watcher)  |

---

## 🔗 API Endpoints

### 🔐 Authentication

| Method | Route                 | Description                 |
|--------|-----------------------|-----------------------------|
| POST   | `/api/register`       | Register new user           |
| POST   | `/api/login`          | Login and get token         |
| POST   | `/api/forgot-password`| Request reset email link    |
| POST   | `/api/reset-password` | Reset password via token    |

---

### 📚 Blog Post Management (🔐 Protected)

| Method | Route             | Description         |
|--------|------------------|---------------------|
| GET    | `/api/posts`      | Get all posts       |
| GET    | `/api/posts/:id`  | Get single post     |
| POST   | `/api/posts`      | Create new post     |
| PUT    | `/api/posts/:id`  | Update a post       |
| DELETE | `/api/posts/:id`  | Delete a post       |

> 🛡️ **Note**: All blog routes require `Authorization` header:  
> `Bearer <your_token>`

---

## ✉️ Forgot Password Flow

1. User hits `POST /api/forgot-password` with email.
2. Mail with reset token link is sent.
3. User clicks link → hits `POST /api/reset-password/:token`.
4. User sets a new password successfully.

---

## 🔒 Security Highlights

- 🧂 **Passwords hashed** using `bcryptjs`
- 🛡️ **Helmet** used to secure HTTP headers
- ✅ **JWT-based route protection**
- 🎯 **Input validation** with `Joi`

---

