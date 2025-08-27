# Fedora Workstation Setup with Ansible

An automated Fedora workstation configuration using Ansible playbooks. This repository provides a streamlined way to set up a complete Fedora desktop environment with gaming capabilities.

## Configured roles

* Common - Install Brave browser, Thunderbird, code editor, Obsidian, Discord, Spotify and Bitwarden

* Nvidia - Install nvidia drivers

* Gaming - Install Steam, Heroic Games launcher and helper software

* Sway - Install and configure Sway DE

## Usage

Run playbook with:

```bash 
ansible-playbook -i inventory playbook.yml --ask-become-pass
```

To install specific role use tags

```bash
ansible-playbook -i inventory playbook.yml --ask-become-pass --tags nvidia
```

To run everything except selected roles use skip tags

```bash
ansible-playbook -i inventory playbook.yml --ask-become-pass --skip-tags nvidia
```