# Ansible User & Group Management Playbook

This Ansible playbook automates the process of creating user groups, users, and applying basic security restrictions such as password policies and forced password resets.  

## 🚀 Features

- Creates a list of groups for each user.
- Creates users and assigns them to their own group.
- Adds users to the **wheel** group for sudo privileges.
- Sets a default hashed password (`pa$$w0rd`).
- Configures password aging policies:
  - **Max days** before password expires: `42`
  - **Min days** before password can be changed: `3`
  - **Warning** before expiration: `35 days`
  - **Account disable** after expiry: `10 days`
- Forces users to change password on first login.
