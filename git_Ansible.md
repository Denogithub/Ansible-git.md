# Ansible-git #

---
- hosts: testservers
  become: yes
  vars:
    - ansible_sudo_pass: password
  

  tasks:
    
    - name: Installing Apache2.It worked!!
      yum:
        name: httpd
        state: installed

    - name: Enable and start the apache service. it works!!    
      service:
        name: httpd
        enabled: yes
        state: started
