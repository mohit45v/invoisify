# Invoisify

Invoisify is a full-stack web application for seamless invoice creation, previewing, history tracking, and sharing. It features a modern React frontend with a Node.js/Express/MongoDB backend, Google OAuth, PDF generation, and supports features like email delivery and custom invoice templates.

---

## Features

- User authentication (local and Google OAuth)
- Invoice creation, preview & export (PDF)
- Invoice history and review system
- Email/send invoices directly
- Responsive modern UI
- Customizable invoice templates

---

## Tech Stack

**Frontend:**
- React (with Vite)
- Redux Toolkit
- React Router DOM
- Material UI, DaisyUI, Bootstrap, TailwindCSS
- Axios, AOS, jsPDF, and more

**Backend:**
- Node.js + Express
- MongoDB (Mongoose ODM)
- Passport + OAuth
- Cloudinary, Multer (file handling)
- EJS (for backend email/views)
- Nodemailer (for email)

---

## Folder Structure

```
backend/   # Node.js/Express + MongoDB REST API
frontend/  # React + Vite single-page app
```

---

## Getting Started

### Prerequisites
- Node.js >= 18.x
- npm (included with Node)
- MongoDB instance (local or Atlas)

### 1. Clone the repository
```bash
git clone <repo_url>
cd invoisify
```

### 2. Setup Backend
```bash
cd backend
npm install
# Create a .env file with necessary variables (see below)
npm run dev   # or: npm start
```

**.env Example:**
```
PORT=8001
SERVER_HOST=localhost
MONGODB_URL=<your-mongo-connection-string>
CORS_ORIGIN=http://localhost:5173
GOOGLE_CLIENT_ID=<get-from-google>
GOOGLE_CLIENT_SECRET=<get-from-google>
SESSION_SECRET=your-session-secret
CLOUDINARY_CLOUD_NAME=...
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...
EMAIL_USER=...
EMAIL_PASS=...
```

Your backend runs at: `http://localhost:8001`

---

### 3. Setup Frontend
```bash
cd ../frontend
npm install
npm run dev
```

Your frontend app runs at: `http://localhost:5173`

---

## API Endpoints

API is RESTful and prefixed with `/api/v1/`. Example routes:
- `/api/v1/user` — User authentication/login/register
- `/api/v1/invoice` — Invoice CRUD operations
- `/api/v1/email` — Email/send invoice
- `/api/v1/review` — Invoice review system
- `/api/v1/template` — Templates management
- `/api/v1/history` — Invoice/activity history

Complete details: see [backend/src/routes/](backend/src/routes/) and controller files for logic.

---

## Contribution
Pull requests are welcome! For major changes, please open an issue first.

---

## License
MIT

---

*Generated with 💻 by Invoisify contributors.*
