# ubuntu config

Update cache, upgrade packages, install default firewall, reboot then check for uptime. Tasks have registered debug output.

#### Quick Start

Clone the repo and then run the playbook as specified

! Don't forget to change the hostname to your own test server e.g. **1.2.3.4** from 10.10.10.10

! **hosts** field is set to **all** to allow host specification via command line

! This playbook works only if you've already set SSH keys as the **root** user e.g. use ssh-copy-id to root@1.2.3.4.

```bash
ansible-playbook -i '10.10.10.10,' ubuntu.yml
```

if you have a hostname/alias already set as inventory, then edit "hosts" entry in file ubuntu.yml from

```bash
- hosts: all
```
to
```bash
- hosts: your_host
```

or you can also set a target variable e.g.

```bash
- hosts: '{{ target }}'
```

and run playbook as:

```bash
ansible-playbook ubuntu.yml --extra-vars "target=your_host"
```
