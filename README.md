# Fedora Workstation Setup with Ansible

An automated Fedora workstation configuration using Ansible playbooks. This repository provides a streamlined way to set up a complete Fedora desktop environment with gaming capabilities.

## Configured roles

* common - Install Brave browser, Thunderbird, VSCode, Obsidian, Discord, Spotify and Bitwarden

* nvidia - Install nvidia drivers

* gaming - Install Steam, Heroic Games launcher and helper software

* sway - Install and configure Sway DE

* jetbrains - Install JetBrains Toolbox

* unity - Install Unity Hub

## Usage

Run playbook with:

```bash 
ansible-playbook -i inventory.yml playbook.yml --ask-become-pass
```

To install specific role use tags

```bash
ansible-playbook -i inventory.yml playbook.yml --ask-become-pass --tags nvidia
```

To run everything except selected roles use skip tags

```bash
ansible-playbook -i inventory.yml playbook.yml --ask-become-pass --skip-tags nvidia
```