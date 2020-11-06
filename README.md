# Ansible Role : Tomcat

Ansible Role for Jakarta Project's Tomcat server.
This roles configures Jakarta's Tomcat through different steps :
- Installs JDK
- Installs Tomcat
- Configures Tomcat

Requirements
------------

- VirtualBox

Example Playbook
----------------

```
- name: Deploy Tomcat for Jakarta
  hosts: "{{ hosts }}"
  remote_user: "{{ user }}"
  tasks:
  - import_role:
      name: tomcat
      tasks_from: install
    vars:
      vm_ip: "{{ tomcat_ip }}"
      vm_name: jakarta_tomcat
      vm_memory: "{{ tomcat_ram }}"
```

Author Information
------------------

* **Toréa TESSIER** - <torea.tessier@reseau.eseo.fr> - [Jakarta Project](https://192.168.4.16/Equipe_1_Jakarta/)