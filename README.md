# UMD Linux Club Server

Server configuration via Ansible for a shared Unix server for the University of
Maryland (UMD) Linux Club.

# Configure server

```sh
ansible-playbook -u root -i "example.com," -e ansible_ssh_port=22 ansible/main.yaml
```

Other arguments potentially useful when testing:

```sh
ansible-playbook -u user -i "localhost," -e ansible_ssh_port=22 -e ansible_become=yes -e ansible_ssh_private_key_file=~/.ssh/umd-linux-server_ed25519 --ask-become-pass ansible/main.yaml
```
