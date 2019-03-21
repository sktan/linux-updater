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

## Contributing
Any pull requests or improvements are welcome, feel free to post any issues as well if you have any suggestions.
