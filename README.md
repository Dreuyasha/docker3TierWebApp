# docker3TierWebApp ******IN PROGRESS******

# 🏗️ Architecture Overview (3-Tier App)

## 🔹 Tier 1 – Presentation Layer

**NGINX (Reverse Proxy)**

* Handles incoming traffic
* Routes requests to backend
* Can handle SSL later
* Runs in its own Docker container

## 🔹 Tier 2 – Application Layer

Example options:

* Flask (Python)
* Node.js (Express)

## 🔹 Tier 3 – Database Layer

Options:

* PostgreSQL

# 🧠 What This Project Demonstrates

✔ Docker networking
✔ Multi-container architecture
✔ Reverse proxy configuration
✔ CI/CD pipeline
✔ Automated Docker builds
✔ Production-style deployment
✔ Infrastructure thinking

# 📦 Final Stack

* NGINX
* Flask
* PostgreSQL
* Docker
* Docker Compose
* Jenkins (running in Docker)

---

# 🔄 High-Level Flow

User → NGINX → Flask App → PostgreSQL


Jenkins Flow:

Push to GitHub →
Jenkins pulls repo →
Runs tests →
Builds Docker images →
Deploys with Docker Compose


---

# 📁 Project Structure

Repo will look like this:


3tier-docker-app/
│
├── app/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── nginx/
│   ├── nginx.conf
│   └── Dockerfile
│
├── db/
│   └── init.sql
│
├── docker-compose.yml
├── Jenkinsfile
└── README.md
