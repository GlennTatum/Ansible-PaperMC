# Ansible-PaperMC
<h4>Ansible Playbook for PaperMC Minecraft Servers</h4>

This playbook is has been tested on and run on a Fedora 36 Server.

Supported Minecraft Versions:

1.18+

<h4>Future features:</h4>

- Systemd Unit File

- Add different version support 1.8-1.18+

- Popular Bukkit Plugins

- Follow the Ansible  <a href="https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html#directory-layout">Directory Layout</a> 

How to use:

1. Add your variables

```
inventory.yaml
---

machines:
  hosts:
    vm01:
      ansible_user: # username
      ansible_host: # Example: 192.168.1.6

      username: "{{ ansible_user }}"
      version: # Example: 1.19
---
```

2. Run the playbook

```
ansible-playbook -i inventory.yaml playbook.yaml -K
```
