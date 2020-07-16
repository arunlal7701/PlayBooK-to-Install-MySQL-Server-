# PlayBooK-to-Install-MySQL-Server-
PlayBooK to Install MySQL Server¶
```
---
- name: "Installing And Configuring MySQL"
  hosts: all
  become: true
  tasks:
    
    - name: "MySQL - Installation"
      apt:
        name: mysql-server
        state: present
          
    - name: "MySQL - Restarting/Enabling"
      service:
        name: mysql
        state: restarted
        enabled: true
