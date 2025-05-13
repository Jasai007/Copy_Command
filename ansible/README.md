# Ansible Commands and Installation

## Installation

### On Ubuntu
```bash
sudo apt update
sudo apt install -y ansible
```

### On CentOS
```bash
sudo yum install -y epel-release
sudo yum install -y ansible
```

## Useful Ansible Commands

- Check Ansible version:
  ```bash
  ansible --version
  ```

- Ping all hosts in inventory:
  ```bash
  ansible all -m ping
  ```

- Run a playbook:
  ```bash
  ansible-playbook <playbook.yml>
  ```

- List all hosts:
  ```bash
  ansible all --list-hosts
  ```

- Check syntax of a playbook:
  ```bash
  ansible-playbook --syntax-check <playbook.yml>
