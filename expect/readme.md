# Automated Linux machine updater

This expect hopes to simplify the patching of linux machines.

**Currently Supports**
* Ubuntu

## How To Use

Create a file with all the hosts you would like to patch.

e.g. my_hosts.txt

```
# Notice the space. This is so that your password is not stored in bash_history
 ./linux_update.exp username my_hosts.txt "password"
```