---
- hosts: all
  become: yes
  tasks:

    # install needed package (method1)
   - name: install postgresql
     ansible.builtin.apt:
      name: postgresql
   - name: install apache web server
     ansible.builtin.apt:
      name: apache2
    
    # install needed package (mathod2)
   - name: install packages
     ansible.builtin.apt:
       name: "{{ item }}"
     loop:
       - postgresql
       - apache2

    # install packages (method 3)
   - name: install packages
     ansible.builtin.apt:
       name:
        - postgresql
        - apache2

   - name: add users
     ansible.builtin.user:
       name: "{{ item }}"
       state: present
     loop:
       - postgres
       - todo
