<p align="center">
  <img width="150" height="150" src="https://upload.wikimedia.org/wikipedia/commons/9/98/WordPress_blue_logo.svg">
</p>

# Ansible Role: WordPress

This project is a fork of [MakarenaLabs/ansible-role-wordpress](https://github.com/MakarenaLabs/ansible-role-wordpress). It includes:
- Addition of Nginx with self-signed HTTPS for testing purposes
- Option to use a custom WordPress archive (backup)
- Example playbook
- Soon: Option to provide a SQL dump for import

[![Build Status](https://travis-ci.org/MakarenaLabs/ansible-role-wordpress.svg?branch=master)](https://travis-ci.org/MakarenaLabs/ansible-role-wordpress)
[![License](https://img.shields.io/github/license/MakarenaLabs/ansible-role-wordpress.svg)](https://opensource.org/licenses/MIT)
[![Ansible Version](https://img.shields.io/badge/ansible-%3E%3D_2.4-8892BF.svg)](https://www.ansible.com/)
[![Ansible Role](https://img.shields.io/ansible/role/36472.svg)](https://galaxy.ansible.com/MakarenaLabs/wordpress/)
[![Ansible Quality](https://img.shields.io/ansible/quality/36472.svg)](https://galaxy.ansible.com/MakarenaLabs/wordpress/)
[![Ansible Downloads](https://img.shields.io/ansible/role/d/36472.svg)](https://galaxy.ansible.com/MakarenaLabs/wordpress/)

Installs and configures the latest version of WordPress.

## Requirements

- Ansible 2.4 or higher

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):
```yaml
wordpress_version: "6.8.1"
wordpress_db_name: "wordpress"
wordpress_db_user: "wordpress"
wordpress_db_password: "wordpress"
wordpress_db_host: "localhost"
wordpress_db_charset: "utf8"
wordpress_db_collate: ""
wordpress_table_prefix: "wp_"
wordpress_debug: false
wordpress_site_url: "http://example.com"
wordpress_home_url: "http://example.com"
wordpress_site_title: "My WordPress Site"
wordpress_admin_user: "admin"
wordpress_admin_password: "password"
wordpress_admin_email: "admin@example.com"
```

## Dependencies

None.

## Example Playbook
```yaml
- hosts: servers
  roles:
    - { role: babidi34.wordpress }
```

## License

MIT

## Author Information

This role was created in 2023 by [babidi34](https://gitlab.com/babidi34).
