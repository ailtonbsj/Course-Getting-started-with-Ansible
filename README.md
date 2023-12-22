# Getting started with Ansible
![](https://img.shields.io/badge/status-progress-blue)

<p align="center">
<img src=".github/logo.png">
</p>

Course from [Learn Linux TV](https://www.youtube.com/@LearnLinuxTV) about [Ansible](https://youtube.com/playlist?list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70&si=4yVFiKpWzec0q8lS).

Creator: Jay LaCroix

## Commands for SSH

```bash
# Create ssh key pair with type ed25519 on ~/.ssh/
ssh-keygen -t ed25519 -C "ansible"

# Copy public key to server
ssh-copy-id -i ~/.ssh/ansible.pub server_ip_or.domain

# Connect with private key
ssh -i ~/.ssh/ansible server_ip_or.domain

# Create process agent to store passphrase
eval $(ssh-agent)

# Add a passphrase to process agent
ssh-add

# Create alias for process agent
# Hint: Add this alias on .bashrc
alias ssha='eval $(ssh-agent) && ssh-add'
```