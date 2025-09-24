# Ansible-git.md #

---
- hosts: testservers
  become: yes
  vars:
    - ansible_sudo_pass: password
  

  tasks:
    
    - name: Installing Apache2
      yum:
        name: httpd
        state: installed

    - name: Enable and start the apache service    
      service:
        name: httpd
        enabled: yes
        state: started
