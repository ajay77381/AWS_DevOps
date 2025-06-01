### What is EC2 ?

Ec2 is a compute capacity that is scalable in Amazon Web Service  cloud. Using Amazon Ec2 eliminate the need to invest in hardware upfront . allowing you to develop and deploy the application more quickly .

Elastic: It is the level at which a system is able to adapt to workload changes by provisioning and de-provisioning resources such that the resources meet the current demand as closely as possible.

# Create Ec2 ?

You have been asked to:
1. Create an Instance in us-east-1 (N. Virginia) region with an Ubuntu OS and install Nginx for making them web servers
2. Change the default website with a hello world page

Step-1 

![Image](https://github.com/user-attachments/assets/2f140950-599f-479d-8f30-6a8c1bf47cef)

Step-2

![Image](https://github.com/user-attachments/assets/e5c62f18-482d-4c25-aca1-8d097ed633ee)

Step-3

![Image](https://github.com/user-attachments/assets/2915e3c9-0937-4d7f-a393-1c3fbfcd64d8)





## Feature of Ec2 -

- Instance are virtual environment 

- Amazon machine image (AMIs) are preconfigured template for your instance the package the bits your need for your server including operating system and additional software 
- Instance type are  different configuration of CPU, memory , storage and networking capacity for your instances.
- Using keypair you can secure you log in information for your instances..


**Elastic**- It is the the level at which system is able to adopt to workload changes by provisioning  and de-provisioning resource which that the resource meet the current demands.

 

## Regions and Availability Zones:

Regions are geographical locations where AWS data-centers reside .Following are AWS region names and their subdivisions:

USEast:N. Virginia(us-east-1),Ohio(us-east-2)

What is Availability zone ?

An AWS availability zone is a logical data centre that is located in certain region. 

For instance, ‘us-east-1’ contains 6 data centers or availability zones:

us-east-1a
us-east-1b
us-east-1c
us-east-1d
us-east-1e
us-east-1f

## Type of Ec2 instance ?

1- General purpose instance
2- Memory optimized
3- Storage optimized
4- Accelerated computing
5- Compute  optimized


What is AMI (  Amazon Machine Image?

Amazon machine image contain the information require to launch the instance 

## Creating and copying an AMI



![Image](https://github.com/user-attachments/assets/787a09dc-50d4-46da-8595-46065773856f)

## Public IP vs Elastic IP

Public IP -
- it is not associated with an AWS account 
- No charges for the public IP even if it not being used while the instance are running
- When ever instance is Re-launched , the public ip  changes.

Elastic IP-

- It is associated with AWS account 
- Charges will be apply if the same is done with the elastic ip
- The elastic ip the same and static every launch until we manually release  it.

How to access the Ec2 machine by ssh cmd ?

Run the cmd and type -
**ssh -i devops.pem ubuntu@12.12.12.12**

where devops.pem is the keypair name , ubuntu is the user name, and after @ it is the ip address for instance.





