# Skill Exchange Platform

A full-stack web application that connects mentors and mentees, enabling skill sharing, goal-based matching, and real-time communication.

---

## 🚀 Features

### Authentication & User Management
- Role-based signup and login (Mentor / Mentee)
- Separate dashboards for each role
- User profile management with role-specific data

### Mentor Features
- Update and showcase skills
- View and manage incoming connection requests (accept/reject)
- Add Zoom/video meeting links for sessions
- Direct message accepted mentees in real time

### Mentee Features
- Set and update learning goals
- Browse mentors matched to their goals
- Send connection requests to mentors
- Direct message accepted mentors in real time

### Matching Engine
- Automatically maps mentee learning goals to mentor skill sets via SQL queries

### Real-Time Messaging
- WebSocket-based (ws library) bidirectional chat
- Persistent chat history stored in MySQL
- Live incoming message display

### Connection Workflow
- Send → Accept/Reject connection request flow
- Zoom meeting link integration on acceptance

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js, Express.js |
| Database | MySQL (mysql2) |
| Real-Time | WebSocket (ws) |
| Other | CORS, REST API |

---

## 📁 Project Structure
Skill_Exchange/
├── server.js                    # Main Express + WebSocket server
├── package.json
├── README.md
└── public/
    ├── index.html               # Landing page
    ├── login.html
    ├── signup.html
    ├── mentor-dashboard.html
    ├── mentee-dashboard.html
    ├── messages.html
    └── admin-dashboard.html


---

## 🗄️ Database Schema

- **users** — stores all user accounts with role info  
- **mentors** — stores mentor skills linked to user ID  
- **mentees** — stores mentee goals linked to user ID  
- **connections** — tracks connection requests and status between mentor-mentee pairs  
- **messages** — stores chat history between users

---

## ⚙️ Getting Started

### Prerequisites
- Node.js (v14+)
- MySQL

### Installation
1. Clone the repository
2. Install dependencies: `npm install`
3. Update DB credentials in `server.js`
4. Run: `node server.js`
5. Open: `http://localhost:3000`

---

## 📡 API Endpoints

Users
- `POST /users` — Create a new user
- `GET /users` — Fetch all users

Mentors
- `POST /mentors` — Update mentor skills
- `GET /mentors/:id` — Fetch mentor skills

Mentees
- `POST /mentees` — Update mentee goals
- `GET /mentees/:id` — Fetch mentee goals

Connections
- `POST /connections` — Send connection request
- `GET /connections/:userId` — Get user connections
- `PUT /connections/:connectionId` — Accept/reject + add Zoom link

Messages
- `POST /messages` — Send a message
- `GET /messages/:userId/:recipientId` — Fetch chat history

