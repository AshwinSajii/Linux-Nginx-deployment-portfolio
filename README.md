# ⚙️ Linux + Nginx Portfolio Website (Hosted on WSL)

This project demonstrates how to **deploy a static HTML portfolio website using Nginx** on **Ubuntu WSL (Windows Subsystem for Linux)**. It includes setup, configuration, troubleshooting, and deployment steps — perfect for System Admins, DevOps learners, or anyone exploring Linux-based web hosting.

---

## 🧠 Project Overview

> A lightweight, dark-themed portfolio built with HTML + CSS and served using **Nginx** on a **WSL Ubuntu environment**.

- 📁 Hosted locally via Nginx (WSL)  
- 🎨 Built with semantic HTML, custom styling, and minimal assets  
- ⚡ Under 5 KiB — optimized for fast loading  
- 💼 Showcases skills in **Linux**, **Shell**, **Cloud**, and **SysAdmin tools**

---

## 🛠️ Technologies Used

| Area                | Stack/Tool                 |
|---------------------|----------------------------|
| OS Environment      | Ubuntu 22.04 (WSL 2)        |
| Web Server          | Nginx                      |
| Language            | HTML5, CSS3 (No frameworks)|
| Hosting (Local)     | http://localhost           |
| Optional            | Git, GitHub Pages (static) |

---

## 🏗️ Setup Instructions

### 1. 🔧 Install Nginx on WSL

```bash
sudo apt update
sudo apt install nginx
ps aux | grep nginx
