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
````

### 2. ✅ Check Nginx is Running

```bash
ps aux | grep nginx
```

You should see the master and worker processes running.

Or visit: [http://localhost](http://localhost)

---

### 3. 📂 Place Your Website Files

Ensure your `index.html` file is ready.

Move it to Nginx's root directory:

```bash
sudo cp index.html /var/www/html/index.html
```

Optionally, replace the default root:

```nginx
# /etc/nginx/sites-enabled/default
server {
    listen 80 default_server;
    root /var/www/html;  # or your custom path
    index index.html;
    ...
}
```

---

### 4. 🔄 Restart Nginx

```bash
sudo nginx -t       # Check config is valid
sudo systemctl restart nginx
```

Now open: [http://localhost](http://localhost)

---

## 🧩 Troubleshooting

### ❌ Port 80 Already in Use

Kill existing processes on port 80:

```bash
sudo lsof -i :80
sudo kill -9 <PID>
```

Then restart Nginx.

---

### 🛑 404 Not Found

* Ensure the `index.html` file is correctly placed at `/var/www/html/`
* Run `ls /var/www/html/` to confirm
* Check permissions:

  ```bash
  sudo chmod 644 /var/www/html/index.html
  ```

---

### 🧠 WSL Tips

* Restart WSL:

  ```bash
  wsl --shutdown
  ```
* Access site via:

  * `http://localhost` (preferred)
  * `http://<WSL_IP>` if needed (use `ip addr`)

---

## 🖥️ Preview Screenshot

<img width="1906" height="865" alt="image" src="https://github.com/user-attachments/assets/7b0169c4-4779-46af-a0b0-5df06ac0fdc2" />


---

## ✍️ Author

**Ashwin Saji**
*System Administrator @ TCS*
Certified: Azure AI-900 | Linux enthusiast
GitHub: [@ashwinsajii](https://github.com/ashwinsajii)

---
 
Let me know if you want me to generate the badge header or anything else!
```
