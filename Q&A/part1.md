ansible : Interview question on modules work based 

1)To skip a task for a specific host, you can use the "--limit" option
and specify the hostname or pattern to match the host you want to skip.

ex: ansible-playbook --limit '!server1' playbook.yml

2)To test the changes made by an ansible playbook without making any actual changes,
 you can use the "--check" flag. This will perform a "dry run" of the playbook and report any 
changes that would be made, but it will not actually make any changes on the target hosts.

ex: ansible-playbook --check playbook.yml

3)To ignore failures and continue running the playbook, you can use the "--force-handlers" flag.
This will cause ansible to continue running the playbook even if a task fails, and it will run
 any handlers (tasks that are triggered by other tasks) that were registered for the failed tasks.

ex: ansible-playbook --force-handlers playbook.yml

4)To skip tasks that would make changes to the target hosts, you can use the "--diff" flag.
 This will perform a "dry run" of the playbook and report any changes that would be made, 
but it will skip any tasks that would make actual changes on the target hosts.

ex: ansible-playbook --diff playbook.yml

5)To skip non-idempotent tasks, you can use the --skip-tags flag and specify the tag or tags for the tasks you want to skip.

ex: ansible-playbook --skip-tags non_idempotent playbook.yml

6)To skip tasks that are not relevant to the target hosts, you can use the "--skip-tags" flag and specify the tag or tags for the tasks you want to skip.

ansible-playbook --skip-tags '!file_server' playbook.yml

7)You can use the command module to run a shell command on all of the servers in your inventory.

- name: Run shell command
  hosts: all
  tasks:
    - name: Run command
      command: echo hello

      
8)You can use the copy module to copy a file from your local machine to all of the servers in your inventory.
         
- name: Copy file
  hosts: all
  tasks:
    - name: Copy file
      copy:
        src: /path/to/local/file
        dest: /path/on/remote/server

      

9)You can use the package module to install a package on all of the servers in your inventory using the package manager for the target operating system.

- name: Install package
  hosts: all
  tasks:
    - name: Install package
      package:
        name: nginx


      
10)You can use the user module to create a user on all of the servers in your inventory.

- name: Create user
  hosts: all
  tasks:
    - name: Create user
      user:
        name: newuser
        password: $6$rounds=656000$somesalt$encryptedpassword
