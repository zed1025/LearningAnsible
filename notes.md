# Terms to remember
- control node
- managed node
- Inventory(Inventory File)
- Playbook
  - Plays
  - Roles(**NOT CLEAR**)
  - Tasks
  - Handler(**NOT CLEAR**)
- Modules(**NOT CLEAR**)
- Plugins(**NOT CLEAR**)
- Collections(**NOT CLEAR**)


# Doubts
- Difference between plays and tasks
- Ansible-Pull
- 


# Notes
- Run playbooks in check mode, `ansible-playbook --check playbook.yml`, this executed the playbook without applying any alterations to your system.
- Verifying playbooks for syntax errors, The ansible-playbook command offers several options for verification, including `--check`, `--diff`, `--list-hosts`, `--list-tasks`, and `--syntax-check`.
- _inventory.ini_ file contains a sample inventory file
  - sample command to test the inventory(using ping module). `ansible -i inventory.ini -u root -m ping all`. All meaning all groups within the inventory. You can also specify individual group names.
  - assigning variables to groups. These variables will be available to the machine in the group
- https://docs.ansible.com/ansible/latest/collections/ansible/builtin/user_module.html
  - Creating a Linux User using ansible adhoc command
    - `ansible -i inventory.ini -u root -m user -a "name=amit state=present" all`
- The package module: https://docs.ansible.com/ansible/latest/collections/ansible/builtin/package_module.html
  - Installing nginx 
    - `ansible -i inventory.ini -u root -m package -a "name=nginx state=present" webservers`
- Ansible Playbooks
  - https://docs.ansible.com/ansible/latest/playbook_guide/index.html
  - 