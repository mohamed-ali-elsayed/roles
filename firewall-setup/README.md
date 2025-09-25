# Ansible Firewall Project

This project installs and configures firewall services on **RedHat** (firewalld) and **Debian** (ufw) systems.

## Inventory
Edit `inventory/hosts.ini` with your servers IPs:
```ini
[red_hat]
192.168.100.11 ansible_user=ansible

[debian]
192.168.100.22 ansible_user=ansible
