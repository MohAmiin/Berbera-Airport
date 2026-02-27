✈️ Airport Operations Automation System

A production-ready full-stack web application designed to digitize manual airport operational checklists, equipment logs, and maintenance reporting into a secure, role-based digital control platform.

Built for internal airport operations management with strict access control and real-time operational tracking.

🚀 Project Overview

The Airport Operations Automation System replaces traditional paper-based equipment checklists with a secure, centralized digital platform.

It supports:

Role-Based Access Control (RBAC)

Shift-based equipment checklists

Automated maintenance reporting

Real-time department statistics

Admin-level operational oversight

Scalable architecture for multi-airport deployment

🏗️ Tech Stack
🔧 Backend

Node.js

Express.js

PostgreSQL

JWT Authentication

bcrypt password hashing

Helmet (Security)

Express Rate Limit

💻 Frontend

Next.js (App Router)

TypeScript

Axios

Responsive Dashboard UI

Control-room styled design

👥 User Roles
Role	Access
ADMIN	Full access to all departments, maintenance reports, and shift resets
STAFF	Access only to assigned department
🏢 Departments

TOWER

AVSEC (Security)

RFF (Fire & Rescue)

OPS (Operations)

Each department has an isolated dashboard.

📊 Core Features
🔐 Authentication & Security

JWT-based login

HTTP-only cookies

bcrypt password hashing

Role-based middleware

Route protection

SQL parameterized queries

🧑‍✈️ Department Dashboard

Shift selection (Morning / Afternoon / Night)

Equipment checklist submission

Status marking:

🟢 Operational

🔴 Faulty (Auto maintenance report)

🟡 Pending

Automatic logging:

Operator name

Timestamp

Shift

Real-time completion statistics

🛠️ Maintenance Management

Automatic maintenance report creation

Equipment status updates

Global admin maintenance overview

Issue tracking

📈 Real-Time Statistics

Completion percentage formula:

Completion % = (Completed Equipment / Total Equipment) × 100

Operational monitoring includes:

Total operational equipment

Equipment under maintenance

Department completion rate

🗄️ Database Schema

Main Tables:

departments

users

equipment

checklist_logs

maintenance_reports

Supports future expansion to multi-airport architecture.

📁 Project Structure
Backend
server/
│
├── src/
│   ├── config/
│   ├── middleware/
│   ├── routes/
│   ├── controllers/
│   ├── services/
│   └── utils/
│
├── server.js
└── .env
Frontend
app/
│
├── login/
├── dashboard/
│   ├── admin/
│   ├── [department]/
│
├── components/
│   ├── Sidebar.tsx
│   ├── EquipmentCard.tsx
│   ├── StatsCard.tsx
│   └── ShiftSelector.tsx
⚙️ Installation
1️⃣ Clone Repository
git clone https://github.com/your-username/airport-ops-system.git
cd airport-ops-system
2️⃣ Backend Setup
cd server
npm install

Create .env:

PORT=5000
DB_HOST=localhost
DB_USER=postgres
DB_PASS=yourpassword
DB_NAME=airport_ops
JWT_SECRET=supersecretkey

Run server:

npm run dev
3️⃣ Frontend Setup
cd airport-ops-client
npm install
npm run dev
🌍 Deployment (Production)

Recommended stack:

Ubuntu 22.04 VPS

Nginx reverse proxy

PM2 process manager

SSL via Certbot

Basic deployment steps:

sudo apt install nginx nodejs postgresql
npm install -g pm2
pm2 start server.js
sudo certbot --nginx
🔒 Security Measures

Password hashing (bcrypt)

JWT expiration (8 hours)

HTTP-only cookies

CORS configuration

Helmet security headers

Rate limiting

Role-based route restrictions

🔮 Future Enhancements

Multi-airport support

AI predictive maintenance

Real-time WebSocket updates

Equipment performance analytics

Mobile application integration

Audit logging system

🤖 Predictive Maintenance Vision

Future model concept:

Failure Rate = Number of Failures / Operating Time

Machine learning can later predict equipment failure based on:

Shift data

Failure frequency

Time between breakdowns

Environmental factors

📌 Roadmap

 Authentication & RBAC

 Department dashboards

 Maintenance automation

 Shift separation

 Multi-airport support

 AI maintenance prediction

 Advanced analytics module

🛫 Use Case

Designed for internal airport operational environments where:

Manual logs slow efficiency

Maintenance tracking needs automation

Shift accountability is required

Admin oversight is critical

Secure role-based isolation is mandatory

📄 License

This project is licensed for internal operational use.

👨‍💻 Author

Mohamed Amiin
Aviation Operations & Systems Development
