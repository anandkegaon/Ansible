In Ubuntu Server Use below mentioned command to install the ansible :

      
    sudo apt-get update
    sudo apt- install software-properties-common -y
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt update
    sudo apt install ansible -y

on hosts // install only python on host system (nodes) //

     sudo apt-get update
    sudo apt-get install python2 -y


generate the ssh key in master and copy paste that key in slave node under.ssh/authorized_keys

command: sudo nano .ssh/authorized_keys
