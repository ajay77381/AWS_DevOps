How to create PDC controller ?

Step-1- Install windows server 2016 standard in system .

The minimum requirements for Windows Server 2016 are:
Processor: 1.4 GHz 64-bit processor
RAM: 512 MB of ECC RAM, or 2 GB for Desktop Environment or Essentials
Hard drive: 32 GB of free space
Network: At least one network card with 1 Gigabit throughput 

Step-2 

Assign the static ip address on NIC with dns address  and change the server name as per planing.

Step-2

Install the ADDS and DNS role form server manager 

Step-3

Click on the flag in the right side of  manage option  Promote the server as a active directory during the selection we need to select create new forest since we are creating the first ADDS .
Like below-

![image](https://github.com/user-attachments/assets/c2f29e04-a607-4f16-ace4-3bae999a8826)


Q1- what are the default path of active directory data base ?

![image](https://github.com/user-attachments/assets/734f5acc-1214-4976-b3d6-c9b00f1beaec)


