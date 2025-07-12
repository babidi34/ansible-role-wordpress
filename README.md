<p align="center">
  <img width="150" height="150" src="https://upload.wikimedia.org/wikipedia/commons/9/98/WordPress_blue_logo.svg" alt="WordPress Logo">
</p>

# Ansible Role: babidi34.wordpress — Deploy WordPress Instantly

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-babidi34.wordpress-2E9AFE.svg)](https://galaxy.ansible.com/babidi34/wordpress)
[![Downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/babidi34/wordpress)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

**A fast, reliable, production-ready Ansible role to deploy and configure WordPress on any Linux server (Debian/Ubuntu, Nginx, Apache, MariaDB/MySQL).**  
Perfect for sysadmins, devops, web agencies, hosting providers and anyone who wants automated, repeatable WordPress installs.

---

## 🚀 Quick install

```bash
ansible-galaxy role install babidi34.wordpress
````

---

## ⚡️ Quick start example

```yaml
- hosts: wordpress_servers
  become: yes
  vars:
    wp_version: "6.8.1"
    wp_sitename: "mysite.fr"
    wp_admin_user: "boss"
    wp_admin_password: "strong_password"
    wp_admin_email: "contact@mysite.fr"
  roles:
    - role: babidi34.wordpress

```

---

## 🎯 Features

* **One-command WordPress deployment** (VM, Cloud, Bare Metal)
* **Nginx, Apache, or Caddy** — choose your stack
* **Automatic HTTPS/SSL setup** 
* **Custom SQL import and backup restore** (bring your own database)
* **100% Open Source** — Fork and contribute!
* **Ready for CI/CD pipelines**

---

## 🔧 Role variables

All variables are customizable (see `defaults/main.yml`). Most common:

```yaml
wordpress_version: "6.8.1"
wordpress_db_name: "wordpress"
wordpress_db_user: "wordpress"
wordpress_db_password: "wordpress"
wordpress_db_host: "localhost"
wordpress_db_charset: "utf8mb4"
wordpress_db_collate: "utf8mb4_unicode_ci"
wordpress_table_prefix: "wp_"
wordpress_site_url: "https://mysite.fr"
wordpress_admin_user: "admin"
wordpress_admin_password: "password"
wordpress_admin_email: "admin@example.com"
wordpress_webserver: "nginx"   # or "apache", "caddy"
wordpress_ssl_enabled: true
wordpress_ssl_certificate: "/etc/ssl/certs/ssl-cert-snakeoil.pem"
wordpress_ssl_certificate_key: "/etc/ssl/private/ssl-cert-snakeoil.key"
```

---

## 📦 Requirements

* Ansible 2.4+ (tested up to 2.18)
* Linux server (Debian 11 and 12 tested)
* SSH access

---

## 💡 FAQ

* **Migration support?**
  Yes, import your SQL dump and wp-content archive for instant restore.
* **Works with Ansible Tower/AWX?**
  Yes, fully compatible.
* **Custom plugins/themes?**
  Just copy files or use extra tasks.
* **Troubleshooting?**
  Open an issue on [GitLab](https://gitlab.com/babidi34/ansible-role-wordpress/issues).

---

## 👨‍💻 Author

Created and maintained by [babidi34 / linux-man](https://gitlab.com/babidi34).
Pull requests and stars welcome!

---

## 📝 License

MIT

---

## ⭐️ *Like this role? Star it on [Galaxy](https://galaxy.ansible.com/babidi34/wordpress) and [GitLab](https://gitlab.com/babidi34/ansible-role-wordpress)!*
