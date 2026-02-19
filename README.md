# MERN Stack Task Manager App

A full-stack Task Manager application built with MongoDB, Express.js, React, and Node.js. Features user authentication, task management, notes, todos, and calendar integration.

---

## 📋 Table of Contents
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Screenshots](#-screenshots)
- [Quick Start](#-quick-start)
- [Project Structure](#-project-structure)
- [Application Flow](#-application-flow)
- [API Flowchart](#-api-flowchart)
- [Environment Variables](#-environment-variables)
- [Deployment](#-deployment)
- [Contact](#-contact)

---

## 🌐 Live Demo

| Component | URL | Status |
|-----------|-----|--------|
| **Frontend** | [https://mern-stack-task-manager-app.vercel.app](https://mern-stack-task-manager-app.vercel.app) | 🟢 Live |
| **Backend API** | [https://task-manager-backend-wm5h.onrender.com](https://task-manager-backend-wm5h.onrender.com) | 🟢 Live |
| **GitHub Repo** | [https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App](https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App) | 📦 Code |

---

## ✨ Features

| Category | Features |
|----------|----------|
| **Authentication** | Local login, Google OAuth, Facebook OAuth, Password Reset |
| **Tasks** | Create, Read, Update, Delete tasks |
| **Notes** | Create, Read, Update, Delete notes |
| **Todos** | Create, Read, Update, Delete todos |
| **Calendar** | View tasks and events in calendar |
| **User Interface** | Dark Mode, Responsive Design, Profile Management |

---

## 🛠️ Tech Stack
Frontend: React.js | React Router | CSS3 | Vercel
Backend: Node.js | Express.js | Passport.js | Nodemailer | Render
Database: MongoDB Atlas

text

---

## 📸 Screenshots

| Login Page | Dashboard View | Tasks View |
|:----------:|:--------------:|:----------:|
| <img src="images/Login.png" width="1000"> |
 <img src="images/Dashboard1.png" width="1000"> |
  <img src="images/Tasks.png" width="1000"> |

| Notes Page | Dashboard View 2 | Features |
|:---------:|:----------------:|:--------:|
| <img src="images/Notes.png" width="1000"> |
 <img src="images/Dashboard2.png" width="1000"> |
  <img src="images/Login.png" width="1000"> |


## 🚀 Quick Start

### Option 1: Use Live App
Simply visit: **https://mern-stack-task-manager-app.vercel.app**

### Option 2: Run Locally

# 1. Clone the repository
git clone https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App.git
cd MERN-Stack-Task-Manager-App

# 2. Setup Backend
cd BackEnd
npm install

# 3. Create .env file in BackEnd folder
Add these variables:
MONGO_URL=your_mongodb_connection_string
SESSION_SECRET=your_secret
JWT_SECRET_KEY=your_jwt_secret
FRONTEND_DOMAIN=http://localhost:3000

# 4. Start Backend Server
npm start

# 5. Setup Frontend (Open a new terminal)
cd FrontEnd
npm install

# 6. Create .env file in FrontEnd folder
# Add this variable:
# REACT_APP_API_URL=http://localhost:8080

# 7. Start Frontend Server
npm start
Access your local app:

Frontend: http://localhost:3000

Backend: http://localhost:8080

📁 Project Structure

MERN-Stack-Task-Manager-App/
│
├── 📂 BackEnd/
│   ├── 📂 Models/               # Database schemas
│   │   ├── Model.js             # User model
│   │   └── DataModel.js         # Tasks/Notes/Todos models
│   ├── 📂 Routes/                # API routes
│   │   ├── TaskRoutes.js
│   │   ├── NoteRoutes.js
│   │   └── TodoRoutes.js
│   ├── 📄 index.js               # Main server file
│   ├── 📄 passport.js            # OAuth configuration
│   └── 📄 package.json
│
├── 📂 FrontEnd/
│   ├── 📂 public/                 # Static files
│   ├── 📂 src/
│   │   ├── 📂 components/         # React components
│   │   │   ├── 📂 Calendar/
│   │   │   ├── 📂 DarkMode/
│   │   │   ├── 📂 Dashboard/
│   │   │   └── ...
│   │   ├── 📄 App.js
│   │   └── 📄 index.js
│   └── 📄 package.json
│
├── 📂 images/                      # Screenshots
│   ├── Login.png
│   ├── Dashboard1.png
│   ├── Dashboard2.png
│   ├── Tasks.png
│   └── Notes.png
│
└── 📄 README.md


🔄 Application Flow

High-Level Architecture

┌─────────────────────────────────────────────────────────────┐
│                      CLIENT SIDE                             │
│  ┌─────────────────────────────────────────────────────┐    │
│  │                 React Frontend                       │    │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐   │    │
│  │  │   Login/    │ │  Dashboard  │ │  Tasks/     │   │    │
│  │  │  Register   │ │             │ │  Notes/Todos │   │    │
│  │  └─────────────┘ └─────────────┘ └─────────────┘   │    │
│  │                    │                                │    │
│  │              HTTP Requests (API Calls)              │    │
│  └────────────────────┬────────────────────────────────┘    │
└───────────────────────┼─────────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────────┐
│                      SERVER SIDE                             │
│  ┌─────────────────────────────────────────────────────┐    │
│  │              Express.js Backend                      │    │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐   │    │
│  │  │   Routes    │ │ Controllers │ │  Models     │   │    │
│  │  │  /api/auth  │ │ Business    │ │  Database   │   │    │
│  │  │  /api/tasks │ │ Logic       │ │  Schema     │   │    │
│  │  │  /api/notes │ │ Validation  │ │             │   │    │
│  │  └─────────────┘ └─────────────┘ └─────────────┘   │    │
│  │                    │                                │    │
│  │              Database Queries                        │    │
│  └────────────────────┬────────────────────────────────┘    │
└───────────────────────┼─────────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────────┐
│                      DATABASE LAYER                          │
│  ┌─────────────────────────────────────────────────────┐    │
│  │              MongoDB Atlas                           │    │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐   │    │
│  │  │   Users     │ │   Tasks     │ │   Notes     │   │    │
│  │  │  Collection │ │  Collection │ │  Collection │   │    │
│  │  └─────────────┘ └─────────────┘ └─────────────┘   │    │
│  │  ┌─────────────┐                                   │    │
│  │  │   Todos     │                                   │    │
│  │  │  Collection │                                   │    │
│  │  └─────────────┘                                   │    │
│  └─────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────┘


Detailed Request-Response Flow

User Action (Click Button)
         │
         ▼
┌─────────────────────────┐
│  React Component        │
│  (FrontEnd)             │
│  ┌───────────────────┐  │
│  │ Event Handler     │  │
│  │ fetch() / axios   │  │
│  └───────────────────┘  │
└───────────┬─────────────┘
            │ API Request (GET/POST/PUT/DELETE)
            │ JSON Data
            ▼
┌─────────────────────────┐
│  Express Route          │
│  (BackEnd)              │
│  ┌───────────────────┐  │
│  │ app.get('/api/')  │  │
│  │ app.post('/api/') │  │
│  └───────────────────┘  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  Controller Function    │
│  (Business Logic)       │
│  ┌───────────────────┐  │
│  │ Validation        │  │
│  │ Error Handling    │  │
│  │ Data Processing   │  │
│  └───────────────────┘  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  MongoDB Model          │
│  (Database Query)       │
│  ┌───────────────────┐  │
│  │ find()            │  │
│  │ save()            │  │
│  │ updateOne()       │  │
│  │ deleteOne()       │  │
│  └───────────────────┘  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  MongoDB Atlas          │
│  (Database)             │
│  ┌───────────────────┐  │
│  │ Data Storage      │  │
│  │ CRUD Operations   │  │
│  └───────────────────┘  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  Response (JSON Data)   │
│  ┌───────────────────┐  │
│  │ Success/Error     │  │
│  │ Requested Data    │  │
│  │ Status Code       │  │
│  └───────────────────┘  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐
│  React Component        │
│  (Update UI)            │
│  ┌───────────────────┐  │
│  │ setState()        │  │
│  │ Re-render         │  │
│  │ Display Data      │  │
│  └───────────────────┘  │
└─────────────────────────┘


📊 API Flowchart

                    ┌─────────────────┐
                    │  Client Browser │
                    └────────┬────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
        ▼                    ▼                    ▼
┌───────────────┐    ┌───────────────┐    ┌───────────────┐
│  GET Request  │    │  POST Request │    │ PUT/DELETE    │
│  /api/tasks   │    │  /api/login   │    │ /api/note/:id │
└───────┬───────┘    └───────┬───────┘    └───────┬───────┘
        │                    │                    │
        └────────────────────┼────────────────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   Express.js    │
                    │    Server       │
                    └────────┬────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
        ▼                    ▼                    ▼
┌───────────────┐    ┌───────────────┐    ┌───────────────┐
│ Authentication│    │  Task/Note/   │    │  Passport.js  │
│   Middleware  │    │  Todo Routes  │    │    OAuth      │
└───────┬───────┘    └───────┬───────┘    └───────┬───────┘
        │                    │                    │
        └────────────────────┼────────────────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   Controller    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │    MongoDB      │
                    │    Models       │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │  MongoDB Atlas  │
                    │   Database      │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   JSON Response │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │  Client Browser │
                    │  (UI Updated)   │
                    └─────────────────┘



🔧 Environment Variables
Backend (.env in BackEnd folder)

MONGO_URL=mongodb+srv://username:password@cluster.mongodb.net/dbname
SESSION_SECRET=your_random_secret_key_here
JWT_SECRET_KEY=your_random_jwt_secret_here
FRONTEND_DOMAIN=http://localhost:3000
Frontend (.env in FrontEnd folder)

REACT_APP_API_URL=http://localhost:8080
Production Variables (on Render/Vercel)

# Render (Backend)
MONGO_URL=your_production_mongodb_url
SESSION_SECRET=production_secret
JWT_SECRET_KEY=production_jwt_secret
FRONTEND_DOMAIN=https://mern-stack-task-manager-app.vercel.app

Vercel (Frontend)
REACT_APP_API_URL=https://task-manager-backend-wm5h.onrender.com

📞 Contact
Mamta Gangwar

GitHub: @Mamta-gangwar

Project Link: https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App

⭐ Support
If you found this project helpful, please give it a star on GitHub!

<p align="center"> <a href="https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App/stargazers"> <img src="https://img.shields.io/github/stars/Mamta-gangwar/MERN-Stack-Task-Manager-App?style=for-the-badge&color=yellow" alt="Stars"> </a> <a href="https://github.com/Mamta-gangwar/MERN-Stack-Task-Manager-App/network/members"> <img src="https://img.shields.io/github/forks/Mamta-gangwar/MERN-Stack-Task-Manager-App?style=for-the-badge&color=blue" alt="Forks"> </a> </p>
<p align="center"> Made with ❤️ by Mamta Gangwar <br> Copyright © 2026 </p> 