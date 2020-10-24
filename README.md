# HotFixUpdate

A Quick Ansible script to fix up Update issues on Amazon Linux issus hosted on ec-2 instances.

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

# Check for packages that need updates

ansible all -i inventory -m yum -a "name='*' state=latest update_cache=true" -s

