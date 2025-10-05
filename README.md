# E-Commerce App — Chapter 1 (Project Setup & Architecture)

This is the starter scaffold for the E-Commerce mastery project.

## Quick start (Windows + VS Code)

Prereqs:
- Java 21 (JDK)
- Maven
- Node.js + npm
- Docker Desktop
- VS Code & Git

1. Clone

git clone <your-repo-url> ecommerce-app
cd ecommerce-app

2. Build backend & run locally
cd backend
mvn clean package -DskipTests
java -jar target/*.jar
# or with Docker
docker build -t ecommerce-backend:local .
docker run -p 8080:8080 ecommerce-backend:local

3. Run frontend (dev)
cd frontend
npm install
npm run dev
# open http://localhost:5173

4. Run full stack with Docker Compose

From repo root:

docker compose up --build
# Frontend -> http://localhost:3000
# Backend API -> http://localhost:8080/api (health at /health)

Notes

This chapter provides skeletons only (health endpoint). We'll implement user auth, product catalog, cart, orders, payments, tests, CI/CD, Helm, monitoring in subsequent chapters.

Use this branch as chapter-1 in git and open PR when ready to move on.


---

# 6 — PowerShell commands to create files & run (copy/paste)

Run these in **PowerShell** from an empty folder where you want `ecommerce-app`:

```powershell
# create directories
mkdir ecommerce-app; 
cd ecommerce-app
mkdir backend; 
mkdir -p backend/src/main/java/com/ecommerce/controller; 
mkdir backend/src/main/resources
mkdir frontend; 
mkdir frontend/src

# create files (you can paste the contents I provided into these files using VS Code)
code .

# (Alternatively use echo >> files but it's faster to paste in VS Code)
