# 🗂️ Dropit Backend

Dropit Backend is the server-side of **Dropit**, a modern cloud storage platform where users can securely upload, manage, and share their files. Built with **NestJS**, **PostgreSQL**, and **Prisma ORM**, it provides robust file storage, authentication, sharing, and tagging features — all powered by a modular monolithic REST architecture.

---

## 🚀 Tech Stack

- **Framework:** NestJS  
- **Database:** PostgreSQL  
- **ORM:** Prisma  
- **Auth:** JWT (Access & HTTP-only Refresh Tokens)  
- **Cache / Rate-Limiting:** Redis  
- **File Handling:** Local uploads (`/uploads/` directory)  
- **Deployment:** Compatible with Render, Railway, or custom servers  

---

## ✨ Key Features

✅ Secure authentication with access & refresh tokens  
✅ Google OAuth login integration  
✅ File upload, download, and preview (images, videos, etc.)  
✅ Create and manage folders  
✅ Soft delete (Trash) and permanent delete  
✅ Favourites system  
✅ File and folder sharing between users  
✅ Search & filter by name, type, tag, or date  
✅ File tagging with custom user-created tags  
✅ Storage quota tracking and detailed usage stats  
✅ Modular structure with clean separation of concerns  

---

## 🧩 Project Structure

src/
├── auth/ # Authentication (JWT + Google OAuth)
├── users/ # User management
├── files/ # File handling (upload, download, delete)
├── folders/ # Folder creation & sharing
├── favourites/ # Favourites system
├── trash/ # Soft deletion (Trash)
├── tags/ # File tagging and search
├── common/ # Shared modules & interceptors
└── main.ts # App entry point


---

## 🛠️ Setup & Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/dropit-backend.git
cd dropit-backend

2️⃣ Install Dependencies

npm install

3️⃣ Generate Prisma Client

npx prisma generate

4️⃣ Run Database Migrations

npx prisma migrate dev

5️⃣ Start the Server

npm run start:dev

The API will be available at:
👉 http://localhost:3001
🧠 API Overview
Feature	Endpoint	Method
Register	/auth/register	POST
Login	/auth/login	POST
Google Login	/auth/google	GET
Refresh Token	/auth/refresh	POST
Upload File	/files/upload	POST
List Files	/files	GET
Delete File	/files/:id	DELETE
Restore File	/trash/restore/:id	PATCH
Share File	/share/:id	POST
Favourite	/favourites/:id	POST
Create Tag	/tags	POST
⚙️ Environment Variables

The backend uses the following environment variables for configuration:
Database Configuration

    DB_HOST

    DB_PORT

    DB_USER

    DB_PASS

    DB_NAME

Application Configuration

    APP_PORT

    APP_ENV

Authentication Configuration

    JWT_ACCESS_SECRET

    JWT_ACCESS_EXPIRATION

    JWT_REFRESH_SECRET

    JWT_REFRESH_EXPIRATION

    JWT_REFRESH_HASH_SECRET

    PASSWORD_SECRET

Redis Configuration

    REDIS_HOST

    REDIS_PORT

API Keys

    API_KEY

    THIRD_PARTY_SERVICE_URL

    CLIENT_URL

Optional: Email Service

    EMAIL_HOST

    EMAIL_PORT

    EMAIL_USER

    EMAIL_PASS

Google OAuth

    GOOGLE_CLIENT_ID

    GOOGLE_CLIENT_SECRET

    GOOGLE_CALLBACK_URL

🧪 Testing

You can test endpoints with Postman or Thunder Client.
Make sure to include your Bearer <ACCESS_TOKEN> for protected routes.
🧱 Scripts

npm run start          # Start production build
npm run start:dev      # Start in dev mode (watch)
npm run build          # Compile the project
npm run test           # Run tests
npm run lint           # Run linter

🧰 Useful Commands

npx prisma studio       # Visual database browser
npx prisma migrate dev  # Apply migrations

📦 Deployment

This project can be deployed on: Railway

👨‍💻 Author

Ahmed Abdelnaby
🧑‍💻 Software Engineer — NestJS | NextJS | PostgreSQL
📍 Egypt
