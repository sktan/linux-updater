# Linux OS Patcher (LOSP)
The Linux OS Patcher is used to quickly update a bunch of linux hosts and restart them.

## Installation
You will require the following tools:

- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Supports
This currently supports the following modern linux distributions below:
- Debian Based (Ubuntu)
- RHEL based (CentOS, Amazon)

## Usage
First, change the os_patcher.yml entry for user to your specified user.

Copy hosts_example into a new file called hosts and add all your servers.
```bash
# Copy hosts_example to hosts and add hosts to file
cp hosts_example hosts
vi hosts

# execute by running:
ansible-playbook -i hosts os_patcher.yml -v
```

### Running on WSFL

```
# Setup SSH with key-agents
$(ssh-agent)
ssh-add ~/.ssh/id_rsa
# Enforce Ansible configuration file
export ANSIBLE_CONFIG="$(pwd)/ansible.cfg"

# Execute patching (Python 3)
python3 /usr/bin/ansible-playbook -i hosts os_patcher.yml -e 'ansible_python_interpreter=/usr/bin/python3' -e 'ansible_ssh_user=ec2-user'
# Execute patching (Python 2)
ansible-playbook -i hosts os_patcher.yml -e 'ansible_ssh_user=ec2-user'
```

## Contributing
Any pull requests or improvements are welcome, feel free to post any issues as well if you have any suggestions.
