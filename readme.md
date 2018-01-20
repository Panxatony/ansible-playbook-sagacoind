# Sagacoind Ansible Playbook Installation

This playbook can be used to install sagacoind Masternodes on Ubuntu 16.04 Linux System

Requirements:

 - Ubuntu Linux 16.04 with python installed -> `apt-get install python`


Installation steps:

1. Deploy virtual machine with python package installed
2. Update `hosts` file and playbook variables in `config-saga-masternode.yml`
3. execute Ansible playbook

```bash
ansible-playbook -i hosts config-saga-masternode.yml --ask-pass`
```

4. Login Server and execute Firewall script 

```bash
/usr/local/bin/firewall.sh
```

5. Switch to saga1 user

```bash
su - saga1
```

Execute installation steps described as Sagacoin

https://sagacoin.net/masternode.html

Masternode wallet needs 2500 Coins to join the masternode network!!!

:-)

This playbook is work in progress. Next steps.

- Add vultr ansible role https://github.com/tundrax/ansible-vultr
- execute firewall config during playbook run

