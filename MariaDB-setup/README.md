# MariaDB Setup with Ansible

This project uses Ansible to install and configure MariaDB on managed nodes.  
Passwords are stored securely using **Ansible Vault**.

## Features

- Installs MariaDB server on RedHat and Debian systems.
- Installs `python3-PyMySQL` automatically (required for Ansible MySQL modules).
- Configures root password securely (only on first run).
- Creates `companydb` database.
- Creates two users with different privilege levels.
- Removes test database and anonymous users.

## Usage

Encrypt your variables file:

```bash
  ansible-vault encrypt MariaDB-setup-role/vars/main.yml

Store your vault password in a hidden file (example ~/.hidden_file).

Run the playbook with:

```bash
  ansible-playbook -i inventory/hosts.ini playbook.yml --vault-password-file ~/.hidden_file
