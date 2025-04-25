🪶 BlogNest API
BlogNest API is a powerful and secure backend service for a blogging platform. Built with Node.js, Express.js, and MongoDB, it provides seamless authentication, blog management, and secure route handling using modern tools like JWT, bcryptjs, and Helmet for security.

🚀 Live Preview (if hosted)
Coming Soon – Deploy on platforms like Render, Railway, or Vercel backend to get a public URL.

📸 Preview
Here's a sneak peek of what the API offers under the hood:

pgsql
Copy
Edit
🔐 Secure JWT Authentication
🧾 RESTful API Design
✉️ Password Reset via Email
🛡️ Helmet + Joi for security & validation
📦 Scalable Code Architecture
🧰 Tech Stack

Category	Technology
Backend	Node.js, Express.js
Database	MongoDB (Mongoose ODM)
Auth	JWT, bcryptjs
Security	Helmet, Cookie-Parser, CORS
Validation	Joi
Mail	Nodemailer
Misc	dotenv, express.json(), nodemon (dev)
📁 Project Structure
bash
Copy
Edit
blognest-api/
├── controllers/        # Auth and Post logic
├── models/             # User and Post schemas
├── routes/             # API route definitions
├── middleware/         # Auth middleware
├── utils/              # (Optional) Email configs, etc.
├── index.js            # Entry point
├── .env                # Secrets & Config
├── package.json
🔧 Installation & Setup
bash
Copy
Edit
git clone https://github.com/your-username/blognest-api.git
cd blognest-api
npm install
🛠️ Create a .env file in root:
env
Copy
Edit
PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_jwt_secret
MAIL_USER=your_email@example.com
MAIL_PASS=your_email_password_or_app_password
🚦 Scripts

Command	Description
npm start	Run the app (production)
npm run dev	Run in development with watcher
🔐 API Endpoints
🔑 Auth Routes

Method	Endpoint	Description
POST	/api/register	Register a user
POST	/api/login	Login and get token
POST	/api/forgot-password	Email password reset link
POST	/api/reset-password/:token	Reset via token
📝 Blog Post Routes (Protected)

Method	Endpoint	Description
GET	/api/posts	Get all posts
GET	/api/posts/:id	Get single post
POST	/api/posts	Create post
PUT	/api/posts/:id	Update post
DELETE	/api/posts/:id	Delete post
✅ Token Required in Authorization header:

bash
Copy
Edit
Bearer <your_jwt_token>
✉️ Forgot Password Flow (Nodemailer)
User submits their email at /forgot-password

Receives a reset link in their inbox.

Resets password via token with /reset-password/:token.

🔒 Security Practices
🧂 Passwords hashed with bcryptjs

🛡️ Helmet for setting secure HTTP headers

✅ JWT Auth Middleware for route protection

🎯 Input validation with Joi

🛠️ Future Features
✅ Comment System

🔍 Search & Filter API

📜 Swagger Documentation

🧑‍🤝‍🧑 Role-based Access (Admin, User)

📄 Pagination & Sorting