# Configuration-Management-DevOps-Roadmap-
Configuration Management DevOps Roadmap 
https://roadmap.sh/projects/configuration-management
The goal of this project is to introduce you to the basics of configuration management using Ansible.
- install basic utilities
- nginx
- static HTML
- add ssh key

## Prerequisites
- Ansible installed on your local machine.
- SSH access to the target server(s).

## Inventory
Open inventory and add your server ip, username and path of the ssh key
all:
  hosts:
    <IP>:
      ansible_ssh_user: username
      ansible_ssh_private_key_file: /path/

## Example Playbook Command

To run a playbook, use the following command:

```bash
ansible-playbook -i <inventory_file> <playbook_file> [--tags "<tag_name>"]
```

### Example:

```bash
ansible-playbook -i inventory.yml setup.yml --tags "base"
```
### Example to run all roles:
```bash
ansible-playbook -i inventory.yml setup.yml
```
