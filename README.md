# 🚀 Automate Code Deployment Using CI/CD Pipeline (GitHub Actions)

This project demonstrates setting up a **CI/CD pipeline** to build, test, and deploy a Node.js web app using:
- **GitHub** & **GitHub Actions** for automation
- **Docker** for containerization
- **Docker Hub** for image registry

---

## 🎯 Objective

Automate the full workflow:
> Test → Build Docker image → Push to Docker Hub → Deploy

---

## 🛠️ Tech Stack

- **Node.js** – Sample web app
- **GitHub Actions** – CI/CD automation
- **Docker** – Build and package app
- **Docker Hub** – Store & distribute images

---

## ⚡ Pipeline Overview

The CI/CD pipeline is defined in `.github/workflows/main.yml` and is triggered on every push to the `main` branch.  
It performs the following steps:

1. **Checkout Code**
2. **Install Dependencies**
3. **Run Tests**
4. **Build Docker Image**
5. **Push Docker Image to Docker Hub**
6. **(Optional) Deploy**

---

## 📦 Folder Structure

```
.
├── .github/workflows/      # CI/CD workflow YAML
├── src/                    # App source code
├── Dockerfile
├── package.json
├── README.md
└── ...
```

---

## 🚦 Quick Start

### 1️⃣ Clone the repository

```sh
git clone https://github.com/sandyzayn/app-nodejs.git
cd your-repo
```

### 2️⃣ Install dependencies

```sh
npm install
```

### 3️⃣ Run tests

```sh
npm test
```

### 4️⃣ Run locally

```sh
npm start
```
App should be available at `http://localhost:3000`

### 5️⃣ Build & Run Docker image

```sh
docker build -t sandyzayn/nodejs-demo-app
docker run -p 3000:3000 sandyzayn/nodejs-demo-app
```

---

## ⚙️ GitHub Actions Workflow

The main workflow is defined in [`.github/workflows/main.yml`](.github/workflows/main.yml).

- **Trigger:** On push to `main`
- **Jobs:**
  - Install & cache dependencies
  - Run tests
  - Build Docker image
  - Log in & push image to Docker Hub

**Sample Workflow Steps:**
```yaml
name: CI/CD Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    ...
```

---

## 📸 Screenshots

### 1️⃣ Pipeline Success & Steps
<img width="1914" height="914" alt="Image" src="https://github.com/user-attachments/assets/d00833f6-1525-4cd0-9ec7-cbd2e77f114c" />

### 2️⃣ Build & Push Docker Image
<img width="1880" height="954" alt="Image" src="https://github.com/user-attachments/assets/5f3758aa-c6ff-4186-af3e-903a9c9ee450" />

### 3️⃣ DockerHub Image Upload
<img width="1880" height="974" alt="Image" src="https://github.com/user-attachments/assets/ec8d30c5-8707-4e8c-8df3-49442f1b33ed" />

### 4️⃣ Test Execution
<img width="1919" height="968" alt="Image" src="https://github.com/user-attachments/assets/5b840b40-35a7-4076-9afe-663a084aa6c9" />

### 5️⃣ Final Pipeline Overview
<img width="1919" height="914" alt="Image" src="https://github.com/user-attachments/assets/859fbaa7-ef9c-499e-9742-3ba755871eb9" />

---

## 📑 Deliverables

- ✅ GitHub repo with workflow YAML
- ✅ Automated build, test, and Docker image push
- ✅ Screenshots of pipeline execution

