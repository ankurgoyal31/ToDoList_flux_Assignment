A full-stack task management application built with React and Node.js, featuring user authentication and task management.

[![Node](https://img.shields.io/badge/node-%3E%3D22.16.0-brightgreen.svg)](https://nodejs.org/)

---

## 🚀 Demo

Try the live demo: [https://todolistassignment-production.up.railway.app/](https://todolistassignment-production.up.railway.app/)

---

## ✨ Features

### 🔐 Authentication & Security
- User registration and login with JWT authentication
- Secure password reset via email
- Protected routes and middleware
- Token refresh mechanism

### 📝 Task Management
- Create, read, update, and delete tasks
- Task completion status tracking
- Dashboard with task statistics

### 📊 Dashboard & Analytics
- Task overview with completion rates
- Today's tasks and overdue tasks
- Task statistics (total, completed, pending)
- User profile management

### 📧 Email Integration
- Password reset emails via Nodemailer
- Gmail OAuth2 integration for email
- Secure email delivery

## 🛠️ Tech Stack

### Frontend
- **React 19.1.0** - Modern UI library
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Beautiful icons
- **Zustand** - Lightweight state management
- **Axios** - HTTP client
- **React Hot Toast** - Elegant notifications

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **Nodemailer** - Email sending
- **Express Validator** - Input validation

## 🚀 Getting Started

### Prerequisites
- Node.js (v22 or higher)
- MongoDB database
- A Gmail account with Google OAuth2 enabled and a refresh token generated for email services.  
    [How to create a Gmail OAuth2 refresh token](https://dev.to/chandrapantachhetri/sending-emails-securely-using-node-js-nodemailer-smtp-gmail-and-oauth2-g3a)

### Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/charith0901/ToDoList_Assignment.git
    cd ToDoList_Assignment
    ```

2. **Install server dependencies**
    ```bash
    cd server
    npm install
    ```

3. **Install client dependencies**
    ```bash
    cd ../client
    npm install
    ```

4. **Environment Setup**

    **Server Environment (.env)**
    ```bash
    cd ../server
    cp env.example .env
    ```
    
    Fill in your environment variables:
    ```
    MONGODB_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret_key
    JWT_REFRESH_SECRET=your_refresh_token_secret
    CLIENT_ID=your_google_oauth_client_id
    CLIENT_SECRET=your_google_oauth_client_secret
    REDIRECT_URI=https://developers.google.com/oauthplayground
    REFRESH_TOKEN=your_google_oauth_refresh_token
    EMAIL_USER=your_gmail_address
    VITE_URL=http://localhost:5173
    ```

    **Client Environment (.env)**
    ```bash
    cd ../client
    cp env.example .env
    ```

### 🏃‍♂️ Running the Application

1. **Start the server (development)**
    ```bash
    cd server
    npm run dev
    ```
    Server will run on `http://localhost:3000`

2. **Start the client (development)**
    ```bash
    cd client
    npm run dev
    ```
    Client will run on `http://localhost:5173`

3. **Build for production**
    ```bash
    # Build client
    cd client
    npm run build
    
    # Start server in production
    cd ../server
    npm start
    ```

## 📁 Project Structure

```
ToDoList_Assignment/
├── client/                     # React frontend
│   ├── public/                # Static assets
│   ├── src/
│   │   ├── components/        # React components
│   │   │   ├── auth/         # Authentication components
│   │   │   ├── common/       # Reusable components
│   │   │   ├── dashboard/    # Dashboard components
│   │   │   ├── task/         # Task management components
│   │   │   └── welcome/      # Welcome page
│   │   ├── services/         # API service functions
│   │   ├── store/            # Zustand state management
│   │   └── utils/            # Utility functions
│   ├── package.json
│   └── vite.config.js
├── server/                    # Node.js backend
│   ├── api/                  # Express app setup
│   ├── config/               # Database configuration
│   ├── controllers/          # Route controllers
│   ├── middleware/           # Custom middleware
│   ├── models/               # Mongoose models
│   ├── routes/               # API routes
│   ├── utils/                # Utility functions
│   ├── package.json
│   └── vercel.json          # Vercel deployment config
└── README.md
```

## 🔗 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/forgot-password` - Request password reset
- `POST /api/auth/reset-password` - Reset password with token
- `POST /api/auth/refresh-token` - Refresh JWT token

### Tasks
- `GET /api/tasks` - Get all user tasks
- `POST /api/tasks` - Create new task
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task
- `PATCH /api/tasks/:id/status` - Toggle task completion
- `GET /api/tasks/overview` - Get task overview/statistics
- `GET /api/tasks/overdue` - Get overdue tasks

## 🎨 Features Overview

### Dashboard
- **Task Statistics**: View total, completed, and pending tasks
- **Today's Tasks**: Quick access to tasks due today
- **Overdue Tasks**: Highlighted overdue items
- **Completion Rate**: Visual progress tracking

### Task Management
- **Priority Levels**: Low, Medium, High priority tasks
- **Due Dates**: Set and track task deadlines
- **Tags**: Organize tasks with custom tags
- **Status Tracking**: Mark tasks as complete/incomplete

### User Experience
- **Responsive Design**: Works on all device sizes
- **Toast Notifications**: User-friendly feedback
- **Protected Routes**: Secure access to authenticated features
- **Clean UI**: Modern and intuitive interface

⭐ **Star this repository if you found it helpful!**
