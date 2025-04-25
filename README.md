# 📘 SL-3 Bookstore App

A Django-based online bookstore with a fully custom admin panel. Users can browse, search, and order books, while administrators manage users, books, and orders from a custom-built dashboard — no use of Django's built-in admin interface.

---

## 🚀 Project Overview

This application provides:

- User registration and login  
- Shopping cart and order placement  
- **Custom admin dashboard** for:
  - Managing books  
  - Handling user roles  
  - Viewing and updating orders  
- Dockerized setup for consistent development and deployment environments

---

## 🛠️ Tech Stack

- **Backend:** Django 4+  
- **Frontend:** HTML, CSS, Bootstrap (custom templates)  
- **Database:** SQLite (can switch to Postgres)  
- **Containerization:** Docker  
- **CI/CD:** Jenkins-ready (optional)

---

## 📦 Requirements

- Docker installed on your machine  
- Git for version control  

---

## ⚙️ Setup & Run (Docker Only)

### 1. Clone the Repository

bash
git clone https://github.com/MIHIRGHUMRE/SL-3-Bookstore.git
cd SL-3-Bookstore


### 2. Build and Run with Docker

bash
docker build -t sl3-bookstore .
docker run -p 8000:8000 sl3-bookstore

- App will be available at:
👉 http://localhost:8000

---

## 🧑‍💼 Custom Admin Panel

- URL: http://localhost:8000/admin-panel/

- Accessible only by users with admin/staff roles

- Built entirely with Django templates and views

- Django Admin is NOT used

---

## 🔐 Creating an Admin User

### Run this inside the container:

- bash
- docker exec -it <container_id> python manage.py createsuperuser

### Or pre-load using:

- bash
- docker exec -it <container_id> python manage.py shell
- >>> exec(open('init_admin.py').read())

---

## 🐳 Docker Notes
- Dockerfile: builds the Django web app

- docker-compose.yml: defines the web service and database

- Uses volume mounts for live code reloads

- Accessible at: http://localhost:8000

---

## 🧪 Jenkins (CI/CD)
If Jenkins is configured:

- Add a Jenkinsfile to the root directory

- Suggested pipeline stages:
  - Lint
  - Test
  - Build Docker Image
  - Deploy

---

## 📸 Screenshots
![Screenshot 2025-04-24 202430](https://github.com/user-attachments/assets/4f1a5c28-8e96-4987-8692-4437f3808b0c)
![Screenshot 2025-04-24 202448](https://github.com/user-attachments/assets/2f6e1b5b-63a0-4494-aa1c-6f89ad17e6ba)
![Screenshot 2025-04-24 202503](https://github.com/user-attachments/assets/2b3f2f4c-c477-43c4-bd6a-c299553c3435)
![Screenshot 2025-04-24 202523](https://github.com/user-attachments/assets/023dc6f8-b0ca-4890-bfa8-b89360bf6103)
![Screenshot 2025-04-24 202547](https://github.com/user-attachments/assets/6922b3d5-7a5b-4418-8301-ecbdc2312dd2)
![Screenshot 2025-04-24 202614](https://github.com/user-attachments/assets/233ff7b3-418f-4df1-9728-2a78dea6b4a0)
