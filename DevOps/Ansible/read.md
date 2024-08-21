 # ANSIBLE
---

What is Ansible ?

* Ansible is an open-source configuration managemnet tool.
* Used for configuration management 
* Can solve wide range of anutomation challenges 
* written by Michael DeHaan.
* Named after a fictional communition device, first used by Ursula K. LeGuin in her novel Rocannon's World in 1966.
* In 2015 Red Hat acquired Ansible

Why ansible ?

Ansible is equally popular to puppet you can see the google graph . Popularity is increasing day by day.

![image](https://github.com/user-attachments/assets/31af0dfc-1690-42d5-b691-9259d6bbdb68)

**Advantage of Ansible** ?

Easy to learn 
* Written in pythone
* Easy installation and configuration steps
* No need to install ansible on slave
* Highly scalable

### How does ansible work ?

Instead of going each system ,manually updating we can use ansible to automate the installation using ansible playbook whih are written in very simple language yaml.

**Problem steatment-**

Say josh run an enterprise , want to install new version of Apache Tomcat in all the system

![image](https://github.com/user-attachments/assets/b35e33e5-13d1-4f6f-b6fb-b1cdc1a1ebd7)


Setting up master slave

## Ansible playbook

Playbook have number of plays

play contain task

task calls core or modules

Handler get triggers from notify and executed at the end only once.

![image](https://github.com/user-attachments/assets/c7b28b7f-8872-46ae-bf2f-3f6d148484c0)


## Ansible Roles

An Ansible role is a group of task , files and handlers stored in a standardized file structure. Roles are small functionalities which can be used in independently but only within a playbook
* ANSIBLE play book - organize tasks
* ANSIBLE Role - organize playbook

## Why do we need ANSIBLE Role ?

Roles simplifies writing complex playbooks

Roles allows you to reuse common configuration steps between different types of servers

Roles are flexible and can be easily modified

### Structure of Ansible Role:

![image](https://github.com/user-attachments/assets/68993ec5-4797-4f95-80ea-949464a3ff1d)



# Ansible Archetecher


![image](https://github.com/user-attachments/assets/608f9e38-0643-415c-9e89-84276abf067a)


Modules -

Ansible modules are units of code that can control system resources or execute
system commands

## Installing ANSIBLE on AWS

1- Install ANSIBLE on master

2- Configure ssh access to ANSIBLE host

3- Setting up ANSIBLE host and testing connection


Step-1

Launched two machine ANSIBLE Master and ANSIBLE Slave

![image](https://github.com/user-attachments/assets/45144bef-6294-4211-b795-d360c0604068)

## On Master host machine installed Ansible using below commond-

     sudo apt-get update
    sudo apt install software-properties-common
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt install ansible
    sudo apt-get install python3

![image](https://github.com/user-attachments/assets/8fc3d243-8864-4a05-9be1-0e9c73e6b019)

![image](https://github.com/user-attachments/assets/9e6bc8e2-8de7-4021-8400-5b80a6c6cb16)


## On slave Host machine-

sudo apt-get update

sudo apt-get install python3

................


On master- When we want to connect to slave from master host -

ssh ubuntu@ ip address fo slave host.
 we get error access deny because we need to give access by adding the publick key in slave.

once we have created key an added in slave we able to communite from ansible master machine.

How to create key- 
    1  cd .ssh
    2  ls
    3  ssh-keygen -t rsa
    5  ls
    6  cat id_rsa.pub

###   Now on slave machine i copy the pub key inside authorized_keys
Insert the new entry in the second line of the file. Save and exit.

![image](https://github.com/user-attachments/assets/3935ef72-5a9b-45a0-9230-44ad7f5a4d77)




    7  ssh ubuntu@52.87.235.49

Now i am able to access the slave machine form ANSIBLE master pachine as per below screen shot after adding the created key in slave machine-

![image](https://github.com/user-attachments/assets/c4a34a46-2c86-47a2-b13f-815bf779571b)





## Adding the host name on ansible machine-

sudo nano /etc/ansible/hosts


[production]

Ansible-Slave ansible_ssh_host=172.31.63.32

![image](https://github.com/user-attachments/assets/43597874-5451-4615-acc8-e49a4f579956)








