# Ansible Backup Role

## Overview
This role creates compressed backups of important directories (`/etc`, `/home`, `/var`) on managed nodes.  
Backups are stored in `/backups` with filenames that include the directory name, hostname, and timestamp.

## Usage

Run manually
```bash
ansible-playbook -i hosts.ini playbook.yml
```
Automation with Cron
Schedule the playbook to run automatically, for example every Thursday at 01:00 AM:
```
```bash
crontab -e
```
0 1 * * 4 /usr/local/bin/ansible-playbook -i /root/hosts.ini /root/playbook.yml
```
Notes
Backups remain on each managed node under /backups.
You can change the backup directories and destination in the role variables.
