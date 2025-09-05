# Cloning Amazon site with HTML & CSS

# Online Clone Amazon

A static e-commerce website clone of Amazon, built with **HTML, CSS, and JavaScript**, containerized using **Docker**, and automated with **GitHub Actions CI/CD**.

online-clone-amazon/
│
├── index.html
├── css/
│ └── style.css
├── js/
│ └── script.js
├── Dockerfile
├── docker-compose.yml
├── .github/
│ └── workflows/
│ └── ci-cd.yml
└── README.md

---

## Tools Used
- **Git & GitHub:** Version control and CI/CD integration.
- **Docker & Docker Compose:** Containerizing the web application.
- **GitHub Actions:** Automated workflow for building, testing, and pushing Docker images.
- **Nginx:** Lightweight web server for serving static content.
- **cURL:** Smoke testing of running Docker containers.

---

## Setup & Usage

### Clone the Repository
```bash
git clone https://github.com/<your-username>/online-clone-amazon.git
cd online-clone-amazon

# vim dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html

# docker-compose.yml
version: '3.8'
services:
  web:
    build: .
    ports:
      - "8081:80"

After running this checkout this port number:
Run this link on the browser to get the application.

http://localhost:8081
