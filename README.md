# Multi-Tenant SaaS Platform

This repository contains a **fully containerized Multi-Tenant SaaS platform** developed using **Node.js, PostgreSQL, React, and Docker**.
The system is designed to support **strict tenant isolation**, **role-based access control**, and **project and task management** across multiple tenants.

All application components (**database, backend, and frontend**) can be started together using a **single Docker command**.

---

## 🛠️ Technology Stack

### Backend

* Node.js
* Express.js
* PostgreSQL
* JWT-based authentication
* Role-Based Access Control 

### Frontend

* React (Vite)
* Axios for API communication
* Role-aware UI rendering

### Infrastructure

* Docker
* Docker Compose
---

## 🚀 Running the Application (Required)

### Prerequisites

Ensure the following tools are installed on your system:

* Docker
* Docker Compose

---

### ▶️ Start Services

From the **root directory of the project**, execute:

```bash
docker-compose up -d
```

This command will automatically:

* Launch the PostgreSQL database
* Apply database migrations and seed initial data
* Start the backend API service
* Start the frontend web application

⚠️ **No manual database or environment setup is needed.**

---

## 🌐 Application Access

| Service      | URL                                                                  |
| ------------ | -------------------------------------------------------------------- |
| Frontend     | [http://localhost:3000](http://localhost:3000)                       |
| Backend API  | [http://localhost:5000](http://localhost:5000)                       |
| Health Check | [http://localhost:5000/api/health](http://localhost:5000/api/health) |

---

## 🔐 Authentication & Roles

The platform supports the following user roles:

* **super_admin** – System-wide administrator
* **tenant_admin** – Administrator within a tenant
* **user** – Standard tenant user

All tenant data is **securely isolated**, ensuring no cross-tenant access.

---

## ✨ Key Features

* Tenant registration and authentication
* Role-based user management
* Project creation and management
* Task assignment and tracking
* Secure JWT-based authentication
* Strong multi-tenant data separation
* Fully Dockerized deployment

---

## 🧪 Verifying Functionality

After starting the services:

1. Open the frontend in a browser
2. Log in using the credentials provided in `submission.json`
3. Validate:

   * Tenant-level data isolation
   * Role-based access restrictions
   * Project and task workflows

---

## 🎥 Demo Video

A complete demonstration covering:

* Application architecture overview
* Docker-based startup process
* Multi-tenant behavior
* User, project, and task flows

* Here's the link:
https://drive.google.com/file/d/1VI4yJEyLTX-pg5vrnenFVK7F_cY2hMCe/view?usp=drive_link

---

##  Notes for Reviewers

* The application is fully containerized
* All services start using `docker-compose up -d`
* Database migrations and seed data run automatically

---
