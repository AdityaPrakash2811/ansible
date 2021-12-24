# Ansible

Ansible is an open-source software provisioning, configuration management, and application-deployment tool enabling infrastructure as code.

The code in this repo mainly deals with system configuration.

## Terms to know in Ansible

- **Inventory -** Ansible works against multiple managed nodes or “hosts” in your infrastructure at the same time, using a list or group of lists known as inventory. Basically in this we can group of servers under one name which will help running commands on group of servers together.

- **Playbook** - Ansible Playbooks offer a repeatable, re-usable, simple configuration management and multi-machine deployment system, one that is well suited to deploying complex applications. 

## Getting started

### Prerequisites 
Ensure that master/control node can connect via SSH to the all other ndes/servers to be controlled

### Installation on CentOS 8
```
sudo dnf install -y epel-release
sudo dnf update
sudo dnf install ansible -y
```

### Create Inventory

Move to */etc/ansible/hosts* on master server and add the servers to be contolled.

```
[servers]
<name_of_server> ansible_host=<Server_IP>
```
One can also specify ansible-port here but we are doing that in the code itself. Add as may servers as you may like which might use a similar configuration.

### Contents of the Repo
- Disabling IPv6
- Changing SSH Port
- Firewall configuration
- Adding/Removing SSH Keys

Created related yaml files for all the taks.

### Running the ansible playbooks
```
ansible-playbook <path_to_file>.yaml
```



