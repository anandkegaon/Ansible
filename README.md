# Ansible

Ansible is open source configuration management tool.
It is agentless service , where ansible server and node will connect directly to each other using SSH. which is consider as secure connection. 
It works on Push mechanisum , 
Basically if any updates are available the it will send that updates to all the connected / configured nodes with it.
all servers private ip is mentioned in the Inventry folder of ansible server with those server only it will communicate .
we can create the group of server and to that group we call as children in the hosts file.

