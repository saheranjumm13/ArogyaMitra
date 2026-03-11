# ArogyaMitra – AI Based Fitness & Wellness System

ArogyaMitra is a health assistance platform designed to help users manage their fitness, nutrition, and daily wellness activities. The system uses AI to generate personalized workout plans, diet suggestions, and provides an interactive coaching experience.

The platform consists of a **FastAPI backend** and a **React frontend**, allowing users to interact with AI-powered services through a modern web interface.

---

# Project Highlights

## User Management

* Secure user authentication using **JWT tokens**
* Account registration and login
* User profile management

## Workout Planning

* AI-generated **7-day workout programs**
* Plans created according to user fitness goals
* Workout history storage

## Nutrition Planning

* Personalized **meal plans with macro breakdown**
* Diet recommendations based on user preferences
* Meal plan history tracking

## AI Fitness Coach

* Chat interface for interacting with an AI coach
* Context-aware responses for health and fitness questions

## Progress Monitoring

* Weight logging and progress visualization
* Achievement system for user motivation

---

# Technology Stack

## Backend

* **FastAPI** – API development
* **SQLAlchemy** – ORM for database interaction
* **SQLite** – Local database
* **Groq API** – LLaMA-3 AI model integration
* **JWT Authentication**

## Frontend

* **React**
* **TypeScript**
* **Tailwind CSS**
* **React Router**
* **Axios**

---

# System Architecture

```
User Interface (React)
        |
        | REST API
        v
Backend Server (FastAPI)
        |
        | ORM
        v
Database (SQLite)
        |
        v
AI Services (Groq API)
```

---

# Installation Guide

## 1 Install Backend Dependencies

```bash
cd backend
pip install -r requirements.txt
```

## 2 Install Frontend Dependencies

```bash
cd frontend
npm install
```

## 3 Environment Configuration

Create a `.env` file inside the backend folder.

```
GROQ_API_KEY=your_api_key
SECRET_KEY=your_secret_key
DATABASE_URL=sqlite:///./arogyamitra.db
```

---

# Running the Application

## Start Backend

```bash
cd backend
uvicorn main:app --reload
```

## Start Frontend

```bash
cd frontend
npm run dev
```

Frontend will run on:

```
http://localhost:5173
```

Backend will run on:

```
http://localhost:8000
```

---

# Main API Endpoints

## Authentication

```
POST /token
POST /register
```

## Workout

```
POST /workout/generate
GET /workout/history
DELETE /workout/{id}
```

## Meal Plans

```
POST /meals/generate
GET /meals/history
```

## AI Coach

```
POST /coach/chat
GET /coach/history
```

## Progress Tracking

```
POST /progress/entry
GET /progress/stats
```

---

# Project Structure

```
arogyamitra
│
├── backend
│   ├── main.py
│   ├── database.py
│   ├── schemas.py
│   ├── routers
│   └── services
│
└── frontend
    ├── src
    │   ├── components
    │   ├── pages
    │   └── services
    └── package.json
```

---

# License

This project is released under the **MIT License**.
