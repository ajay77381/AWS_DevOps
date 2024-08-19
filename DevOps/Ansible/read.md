Agenda
---

What is Ansible ?

* Ansible is an open-source configuration managemnet tool.
* Used for configuration management 
* Can solve wide range of anutomation challenges 
* written by Michael DeHaan.
* Named after a fictional communition device, first used by Ursula K. LeGuin in her novel Rocannon's World in 1966.
* In 2015 Red Hat acquired Ansible


why ansible ?

How does ansible work ?

Case study nasa

Setting up master slave

Ansible playbook

Ansible Roles

Using roles in playbook







![image](https://github.com/user-attachments/assets/faa263b3-c333-4c2e-b8bd-619c5aeb0ecb)



# Ansible Archetecher


![image](https://github.com/user-attachments/assets/608f9e38-0643-415c-9e89-84276abf067a)






On Master host machine-

1  sudo apt-get update
    2  sudoapt install software-properties-common
    3  sudo apt install software-properties-common
    4  sudo at-add-repository ppa:ansible/ansible
    5  sudo apt-add-repository ppa:ansible/ansible
    6  sudo apt install ansible
    8  sudo apt-get install python3
    9  ssh ubuntu@44.202.36.119
   10  clear
   11  history




on Slave Host machine-

sudo apt-get update
sudo apt-get install python

................


On master- When we want to connect to slave from master host -

ssh ubuntu@ ip address fo slave host.
 we get error access deny because we need to give access by adding the publick key in slave.

once we have created key an added in slave we able to communite from ansible master machine.

ubuntu@ip-172-31-80-34:~/.ssh$ history
    1  cd .ssh
    2  ls
    3  cat authorized_keys
    4  ssh-keygen
    5  ls
    6  cat id_rsa.pub
    7  ssh ubuntu@44.202.36.119
    8  history


Adding the host name on ansible machine-

sodo nano /etc/ansible/hosts

[production]

Ansible-Slave ansible_ssh_host=44.202.36.119
