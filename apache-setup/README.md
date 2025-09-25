# Ansible Apache Setup Role

## 📌 Overview
This project is an **Ansible role** to install, configure, and manage the Apache HTTP server (`httpd` on RedHat-based systems, `apache2` on Debian-based systems).  
It ensures that Apache is installed, started, enabled on boot, and serves a custom `index.html` page.  
Additionally, it configures the firewall to allow HTTP traffic (port 80).

## ⚙️ Features
- Installs Apache on **RedHat** (`httpd`) and **Debian** (`apache2`) systems.
- Ensures Apache service is **enabled and started** at boot.
- Deploys a sample `index.html` to the default document root `/var/www/html/`.
- Sets correct **ownership and permissions** for RedHat (`apache:apache`) and Debian (`www-data:www-data`).
- Configures firewall:
  - Uses **firewalld** on RedHat.
  - Uses **ufw** on Debian.
