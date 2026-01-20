# Restaurant QR Management Frontend 🚀

A production-ready **React + Vite** frontend application deployed on **AWS S3 and CloudFront** with a **fully automated CI/CD pipeline using GitHub Actions**.

This project demonstrates real-world cloud deployment, automation, and DevOps best practices.

---

## 🔗 Live Demo

🌐 **Deployed via CloudFront (CDN):**  
https://d62ys23woaplt.cloudfront.net

---

## 🏗️ Architecture Overview

User Browser
↓
CloudFront (CDN + HTTPS + Cache)
↓
S3 Bucket (Private Static Files)


- **S3** stores the production build (`dist/`)
- **CloudFront** serves content globally with low latency
- **Origin Access Control (OAC)** ensures S3 is not publicly accessible
- **GitHub Actions** automates build and deployment

---

## ⚙️ CI/CD Pipeline (GitHub Actions)

On every push to the `main` branch:

1. GitHub Actions checks out the code
2. Installs dependencies
3. Builds the Vite project
4. Syncs build output to S3
5. Invalidates CloudFront cache (`/*`)
6. New version is live globally

✅ Zero manual deployment  
✅ Zero downtime  
✅ Fully automated

---

## 🧠 Key Features

- ⚡ Built with **Vite + React + TypeScript**
- ☁️ Hosted on **AWS S3 (private bucket)**
- 🌍 Served via **CloudFront CDN**
- 🔐 Secure access using **Origin Access Control**
- 🔄 SPA routing handled via CloudFront error rules
- 🤖 Automated CI/CD with **GitHub Actions**
- 🛡️ AWS IAM user with programmatic access for CI/CD

---

## 🧰 Tech Stack

- **Frontend:** React, Vite, TypeScript
- **Cloud:** AWS S3, AWS CloudFront, IAM
- **CI/CD:** GitHub Actions
- **Tooling:** AWS CLI, Git, Node.js

---

## 📂 Repository Structure

.
├── .github/workflows/deploy.yml # CI/CD pipeline
├── components/ # UI components
├── pages/ # Application pages
├── services/ # API / service logic
├── contexts/ # React context
├── App.tsx
├── index.tsx
├── vite.config.ts
├── package.json
└── README.md


---

## 🚀 Run Locally

### Prerequisites
- Node.js (v18+ recommended)

### Steps

```bash
git clone https://github.com/akshaysuthar64767/restaurant_qr_managements.git
cd restaurant_qr_managements
npm install
npm run dev

App will run at:

http://localhost:5173
