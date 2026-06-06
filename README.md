<img width="1533" height="891" alt="Diagram (2)" src="https://github.com/user-attachments/assets/9a7d8ea3-6093-4089-a623-953493112d94" />

# Employee Review System

A full-stack Employee Review System built with Node.js, Express, PostgreSQL, Docker, and Nginx, featuring an automated CI/CD pipeline using GitHub Actions and deployment on an Ubuntu Server.

---

## Project Overview

The Employee Review System is a web application designed to streamline employee performance reviews within an organization.

The system allows administrators, managers, and employees to interact through role-based access controls, enabling performance evaluations, feedback management, and review tracking.

In addition to application development, this project focuses on implementing real-world DevOps practices including containerization, automated deployments, infrastructure management, and CI/CD automation.

---

## Features

### Authentication & Authorization

* User Login System
* Session Management
* Role-Based Access Control (RBAC)
* Secure Environment Variable Management

### Employee Management

* Employee Profile Management
* Employee Listing
* Employee Details View

### Review Management

* Performance Reviews
* Manager Feedback
* Review History Tracking
* Review Status Management

### File Management

* File Upload Support
* Document Storage
* Secure File Handling

### Deployment & Operations

* Dockerized Application
* PostgreSQL Persistent Storage
* Nginx Reverse Proxy
* Automated CI/CD Pipeline
* Ubuntu Server Deployment

---

## Technology Stack

### Backend

* Node.js
* Express.js

### Database

* PostgreSQL

### DevOps & Infrastructure

* Docker
* Docker Compose
* GitHub Actions
* Nginx
* Ubuntu Server

### Version Control

* Git
* GitHub

---

## System Architecture

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions (CI/CD)
    │
    ├── Build Application
    ├── Validate Changes
    ├── Build Docker Images
    └── Deploy via SSH
    │
    ▼
Ubuntu Server
    │
    ├── Nginx
    ├── Node.js Container
    └── PostgreSQL Container
    │
    ▼
End Users
```

---

## CI/CD Pipeline

### Continuous Integration

On every push to the repository:

1. GitHub Actions workflow starts.
2. Source code is checked out.
3. Dependencies are installed.
4. Application build is validated.
5. Docker images are created.

### Continuous Deployment

After successful validation:

1. GitHub Actions connects to Ubuntu Server using SSH.
2. Latest code is pulled.
3. Existing containers are stopped.
4. Docker Compose rebuilds services.
5. Updated containers are deployed automatically.

---

## Docker Services

### Application Container

```yaml
Node.js Application
Port: 3000
```

### Database Container

```yaml
PostgreSQL
Port: 5432
Volume: pgdata
```

### Reverse Proxy

```yaml
Nginx
Port: 80
Port: 443
```

---

## Environment Variables

Create a `.env` file:

```env
PORT=3000

DB_HOST=postgres
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=your_password
DB_NAME=employee_review_db

SESSION_SECRET=your_secret
```

---

## Local Development Setup

### Clone Repository

```bash
git clone https://github.com/dharmenderprof-dev/employee-review-system.git

cd employee-review-system
```

### Install Dependencies

```bash
npm install
```

### Start Application

```bash
npm start
```

---

## Docker Setup

### Build Containers

```bash
docker-compose build
```

### Start Services

```bash
docker-compose up -d
```

### View Running Containers

```bash
docker ps
```

### Stop Services

```bash
docker-compose down
```

---

## Production Deployment

### Server Requirements

* Ubuntu Server
* Docker
* Docker Compose
* Git
* Nginx
* SSH Access

### Deployment Process

```bash
git pull

docker-compose down

docker-compose up -d --build
```

---

## Security Measures

* Environment Variables
* SSH Key Authentication
* GitHub Secrets
* Session-Based Authentication
* Nginx Reverse Proxy
* Database Isolation through Docker Network

---

## Learning Outcomes

This project provided hands-on experience with:

* Linux Administration
* Docker Containerization
* Docker Compose Orchestration
* GitHub Actions CI/CD
* PostgreSQL Management
* Reverse Proxy Configuration
* Server Deployment
* Infrastructure Automation
* Production Workflows

---

## Future Improvements

* Health Checks
* Application Logging
* Database Backups
* Prometheus Monitoring
* Grafana Dashboards
* Kubernetes Deployment
* Helm Charts
* Terraform Infrastructure Automation

---

## Author

Dharmender

Aspiring DevOps Engineer | 

---

## License

This project is created for educational and portfolio purposes.
