Installation Part for Master and slave:

In Ubuntu Server Use below mentioned command to install the ansible (Master) :

      
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


on hosts // install only python on (Slave) system (nodes) //

     sudo apt-get update
    sudo apt-get install python3 -y

#######################################################################################

Configuration Part:

try to access slave machine using ssh command ex : " ssh ubuntu@<public_ip_of_slave_machine> "
it will give permssion denied error.

then do below step:

In Master node:
cd .ssh         cd to .ssh
ssh-keygen     generate the public and private key for master node
ls             list the newfiles
cat .pub file  " copy the code and paste it into slave machine under (.ssh/authorized_keys )"

In slave node:
cd .ssh
vi authorized_keys 
paste master .pub key 
save it .



command: sudo nano .ssh/authorized_keys

Ansible ping command


    ansible all  -i invent -m ping -u ubuntu
    

