# my-node-app

# My Node.js CI/CD Pipeline Project

## 🚀 Project Overview
A real-world DevOps project built from scratch using Jenkins, Docker, and GitHub.

## 🛠️ Tech Stack
- **App**: Node.js + Express
- **Testing**: Jest + Supertest
- **CI/CD**: Jenkins
- **Containerization**: Docker
- **Code Repository**: GitHub
- **Platform**: KillerCoda (Ubuntu)

## 📁 Project Structure

my-node-app/
├── app.js
├── package.json
├── Dockerfile
├── Jenkinsfile
└── test/
└── app.test.js

## ⚙️ CI/CD Pipeline Stages
1. **Checkout** - Jenkins pulls code from GitHub
2. **Install** - Installs npm dependencies
3. **Test** - Runs automated tests using Jest
4. **Build Docker Image** - Builds a Docker image of the app
5. **Deploy** - Runs the app in a Docker container on port 3000

## 🐳 Docker
The app runs inside a Docker container:
- Base image: node:18-alpine
- Exposed port: 3000

## ✅ How to Run Locally
```bash
npm install
npm test
npm start
```

## 🔁 How the Pipeline Works
Every time code is pushed to GitHub:
1. Jenkins automatically detects the change
2. Runs all pipeline stages
3. Deploys the latest version inside Docker

##<img width="507" height="81" alt="image" src="https://github.com/user-attachments/assets/fa5ec351-3141-43bb-80fb-fd3fc743d201" />

App responds with:  Hello from my CI/CD Pipeline!

