# HotFixUpdate

Quick Ansible script to fix up Update issues

# Usage

Copy your .pem key in same directory

To run
```bash
ansible-playbook main.yml -i inventory
```


# Update everything

ansible all -i inventory -a "yum update -y" -s

# Update individual packages
ansible all -i inventory -m yum -a "name=git state=latest update_cache=true" -s

