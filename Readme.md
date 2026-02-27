# ✈️ Airport Operations Automation System

![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Framework-Express.js-000000?logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791?logo=postgresql&logoColor=white)
![Next.js](https://img.shields.io/badge/Frontend-Next.js-000000?logo=next.js&logoColor=white)
![JWT](https://img.shields.io/badge/Auth-JWT-black?logo=jsonwebtokens)
![Security](https://img.shields.io/badge/Security-Role--Based%20Access-blue)
![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)
![License](https://img.shields.io/badge/License-Internal-orange)

---

## 🚀 Overview

The **Airport Operations Automation System** is a production-ready full-stack platform designed to replace manual airport equipment checklists and operational control logs with a secure, role-based digital solution.

This system enables:

- 🔐 Secure authentication and authorization
- 🏢 Department-specific dashboards
- 🛠 Automated maintenance reporting
- 📊 Real-time operational statistics
- 👨‍✈️ Administrative oversight
- 🌍 Scalable multi-airport architecture

---

## 🏗️ System Architecture
Frontend (Next.js)
↓
Backend API (Node.js + Express)
↓
PostgreSQL Database


- JWT authentication (HTTP-only cookies)
- Role-Based Access Control (RBAC)
- Modular backend structure
- Shift-based logging
- Maintenance automation

---

## 👥 User Roles

| Role  | Permissions |
|-------|------------|
| ADMIN | Full access to all departments, maintenance reports, shift reset, global statistics |
| STAFF | Access only to assigned department dashboard |

---

## 🏢 Departments

- TOWER  
- AVSEC (Security)  
- RFF (Fire & Rescue)  
- OPS (Operations)

Each department operates within its own isolated dashboard.

---

## 📊 Core Features

### 🔐 Authentication & Security
- JWT-based login
- bcrypt password hashing
- HTTP-only secure cookies
- Role-protected routes
- Rate limiting
- Helmet security headers
- Parameterized SQL queries

---

### 🧑‍✈️ Department Dashboard

- Shift selection:
  - Morning
  - Afternoon
  - Night
- Equipment checklist submission
- Status marking:
  - 🟢 Operational
  - 🔴 Faulty (Auto maintenance report)
  - 🟡 Pending
- Automatic logging:
  - Operator name
  - Timestamp
  - Shift

---

### 🛠 Maintenance Automation

When equipment is marked as faulty:

- Status updates to **Under Maintenance**
- Maintenance report automatically created
- Admin can monitor all maintenance cases

---

### 📈 Real-Time Statistics


Completion % = (Completed Equipment / Total Equipment) × 100


Dashboard shows:

- Total departments
- Total equipment
- Operational equipment
- Equipment under maintenance
- Shift completion percentage

---

## 🗄️ Database Schema

Main Tables:

- departments
- users
- equipment
- checklist_logs
- maintenance_reports

Database is structured for future multi-airport scalability.

---

## 📁 Project Structure

### Backend


server/
│
├── src/
│ ├── config/
│ ├── middleware/
│ ├── routes/
│ ├── controllers/
│ ├── services/
│ └── utils/
│
├── server.js
└── .env


### Frontend


app/
│
├── login/
├── dashboard/
│ ├── admin/
│ ├── [department]/
│
├── components/
│ ├── Sidebar.tsx
│ ├── EquipmentCard.tsx
│ ├── StatsCard.tsx
│ └── ShiftSelector.tsx


---

## ⚙️ Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/airport-ops-system.git
cd airport-ops-system
2️⃣ Backend Setup
cd server
npm install

Create .env file:

PORT=5000
DB_HOST=localhost
DB_USER=postgres
DB_PASS=yourpassword
DB_NAME=airport_ops
JWT_SECRET=supersecretkey

Run backend:

npm run dev
3️⃣ Frontend Setup
cd airport-ops-client
npm install
npm run dev
🌍 Production Deployment

Recommended production stack:

Ubuntu 22.04 VPS

Nginx reverse proxy

PM2 process manager

SSL via Certbot

sudo apt install nginx nodejs postgresql
npm install -g pm2
pm2 start server.js
sudo certbot --nginx
🔒 Security Checklist

✔ bcrypt hashing

✔ JWT expiration (8 hours)

✔ HTTP-only cookies

✔ CORS configuration

✔ Helmet headers

✔ Rate limiting

✔ Role middleware

✔ Input validation

🔮 Future Enhancements

Multi-airport support

AI predictive maintenance

WebSocket real-time updates

Advanced analytics dashboard

Audit logging system

Mobile integration

📌 Roadmap

 Authentication & RBAC

 Department dashboards

 Shift-based checklist

 Maintenance automation

 Multi-airport support

 AI maintenance prediction

 Advanced analytics module

👨‍💻 Author

Mohamed Amiin
Aviation Operations & Systems Development

📄 License

Internal operational use only.
