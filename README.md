
# Linux & Nginx Portfolio Website

## Overview
This is a simple, professional portfolio website built with HTML, styled with CSS for a dark theme, and served using **Nginx** on Linux or WSL environments. It showcases skills, projects, certifications, and contact info — optimized to be under 5KB for fast loading.

---

## How to Run Locally (Linux/WSL)

### 1. Copy your `index.html` to the Nginx web root:
```bash
sudo cp ~/my-nginx-site/index.html /var/www/html/index.html
````

### 2. Test Nginx configuration:

```bash
sudo nginx -t
```

### 3. Restart Nginx:

```bash
sudo systemctl restart nginx
```

### 4. Open your browser and go to:

```
http://localhost
```

---

## Troubleshooting

### 404 Not Found Error

* Ensure your `index.html` is inside `/var/www/html/`
* Check your Nginx config root path:

  ```bash
  cat /etc/nginx/sites-enabled/default | grep root
  ```
* Run `sudo nginx -t` to check syntax.
* Restart Nginx after changes.

### Nginx Bind Errors (`Address already in use`)

* Check if port 80 is in use:

  ```bash
  sudo lsof -i :80
  ```
* Kill the process holding the port or stop conflicting services:

  ```bash
  sudo kill <PID>
  ```
* Then restart Nginx.

### Changes Not Reflecting After Refresh

* Clear your browser cache or do a hard reload (Ctrl+Shift+R or Cmd+Shift+R)
* Confirm your `index.html` was updated in `/var/www/html/`

---

## WSL Tips

* Run Nginx with `sudo` inside WSL.
* Use `systemctl` commands or start Nginx manually:

  ```bash
  sudo nginx
  ```
* Access via `localhost` or `127.0.0.1` in your Windows browser.

---

## Author

Ashwin Saji
*System Administrator @ TCS*
Cloud & AI Enthusiast | Linux & Shell Scripting Learner
[GitHub](https://github.com/ashwinsajii) | [LinkedIn](https://www.linkedin.com/in/ashwinsajii)

---

## Future Ideas

* Add dynamic content with JavaScript or backend (Node.js/PHP)
* Automate deployment scripts with shell scripting
* Integrate CI/CD pipelines for automated updates
* Explore containerizing the app with Docker
* Expand portfolio with more projects and certifications

```

That will create a `README.md` file with all the content you want.

---

If you want to do the **same** for your `index.html` file, just replace `README.md` with `index.html` and paste the HTML code inside the here-doc.  
Want me to help with that too?
```
