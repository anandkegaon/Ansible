In Ubuntu Server Use below mentioned command to install the ansible :

      
    sudo apt-get update
    sudo apt-get install software-properties-common -y
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt update
    sudo apt install ansible-core
    sudo apt install ansible -y

Normally ansible hosts file , will find under the path "/etc/ansible/hosts"
if the path is not availble after installing the ansible the we can create it manually

    mkdir /etc/ansible
    cd /etc/ansible
    vi hosts
and write the IP address in the hosts file which will act as inventory file.


on hosts // install only python on host system (nodes) //

     sudo apt-get update
    sudo apt-get install python3 -y


generate the ssh key in master and copy paste that key in slave node under.ssh/authorized_keys

command: sudo nano .ssh/authorized_keys

Ansible ping command


    ansible all  -i invent -m ping -u ubuntu
    

