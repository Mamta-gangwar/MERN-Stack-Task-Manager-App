# MERN Stack Task Manager App

A full-stack Task Manager application built with the MERN stack (MongoDB, Express.js, React, Node.js). Features user authentication, task management, notes, todos, and calendar integration.

---

## 🌐 Live Demo

The application is fully deployed and live!

| Component | URL |
|-----------|-----|
| **Frontend Application** | [https://mern-stack-task-manager-app.vercel.app](https://mern-stack-task-manager-app.vercel.app) |
| **Backend API** | [https://task-manager-backend-wm5h.onrender.com](https://task-manager-backend-wm5h.onrender.com) |
| **GitHub Repository** | [https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App](https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App) |

<p align="center">
  <a href="https://mern-stack-task-manager-app.vercel.app">
    <img src="https://img.shields.io/badge/Deployed%20on-Vercel-black?style=for-the-badge&logo=vercel" alt="Vercel">
  </a>
  <a href="https://task-manager-backend-wm5h.onrender.com">
    <img src="https://img.shields.io/badge/Deployed%20on-Render-blue?style=for-the-badge&logo=render" alt="Render">
  </a>
</p>

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| ✅ **User Authentication** | Local, Google, and Facebook login with Passport.js |
| ✅ **Task Management** | Create, edit, delete, and track your daily tasks |
| ✅ **Notes** | Save and organize your important notes |
| ✅ **Todo Lists** | Create and manage todos with checkboxes |
| ✅ **Calendar View** | See all your tasks and events in an interactive calendar |
| ✅ **Dark Mode** | Toggle between light and dark themes |
| ✅ **Password Reset** | Forgot password functionality with email integration |
| ✅ **User Profile** | View and manage your personal profile |

---

## 🛠️ Tech Stack

**Frontend:**
- ⚛️ React.js
- 🚦 React Router
- 🎨 CSS3
- 🚀 Deployed on Vercel

**Backend:**
- 🟢 Node.js
- 🚂 Express.js
- 🍃 MongoDB Atlas
- 🔐 Passport.js (Authentication)
- 📧 Nodemailer (Email service)
- ⚙️ Deployed on Render

---

## 🚀 Quick Start

### **Visit the Live App**
Simply go to: **[https://mern-stack-task-manager-app.vercel.app](https://mern-stack-task-manager-app.vercel.app)**

1. Create a new account
2. Or login with Google/Facebook
3. Start managing your tasks!

### **Run Locally**

# Clone the repository
git clone https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App.git
cd MERN-Stack-Task-Manager-App

# Install backend dependencies
cd BackEnd
npm install

# Create .env file in BackEnd folder
# Add these variables:
# MONGO_URL=your_mongodb_connection_string
# SESSION_SECRET=your_secret
# JWT_SECRET_KEY=your_jwt_secret
# FRONTEND_DOMAIN=http://localhost:3000

# Start backend server
npm start

# In a new terminal, install and start frontend
cd FrontEnd
npm install
npm start

## 📸 **Screenshots**

Here are some screenshots of the Task Manager application:

| **Login Page** | **Dashboard View 1** | **Tasks View** |
|:--------------:|:--------------------:|:--------------:|
| <img src="images/Login.png" width="300"> | <img src="images/Dashboard1.png" width="300"> | <img src="images/Tasks.png" width="300"> |

| **Notes Page** | **Dashboard View 2** | **Login Page (Alt)** |
|:--------------:|:--------------------:|:--------------------:|
| <img src="images/Notes.png" width="300"> | <img src="images/Dashboard2.png" width="300"> | <img src="images/Login.png" width="300"> |

MERN-Stack-Task-Manager-App/
├── BackEnd/               # Node.js/Express backend
│   ├── Models/            # Database models
│   ├── Routes/            # API routes
│   ├── index.js           # Main server file
│   └── package.json
├── FrontEnd/              # React frontend
│   ├── public/            # Static files
│   ├── src/               # React components
│   │   ├── components/    # All React components
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
└── README.md

📞 Contact
Mamta Gangwar

GitHub: @Mamta-gangwar

Project Link: https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App

<p align="center"> Made with ❤️ by Mamta Gangwar <br> ⭐ If you found this project helpful, please give it a star! </p>