
# How to create Ec2 Auto-scaling group ?


Step-1

We need to crate VPC



![Image](https://github.com/user-attachments/assets/5e9d8ff4-65c4-4e09-8e9a-100e749f0b9f)

After create VPC we need to create internet gateway and attach it to VPC-



![Image](https://github.com/user-attachments/assets/647465cb-b118-4f46-94b0-ba4bec2db3e1)



![Image](https://github.com/user-attachments/assets/8471cc31-0e8b-463f-b987-fe2a23b5975a)

Step-2

Now Create the subnet -



![Image](https://github.com/user-attachments/assets/293547e4-c261-48ed-aad7-2b149c45392c)


Step-3
Create the route table and associated with subnet which we have created(two subnet)



![Image](https://github.com/user-attachments/assets/ec50a727-fe67-44d9-ae12-b09ba1a7b487)

We have associated the subnet but our route table also responsible for providing the internet access so in the route section edit the route section and add route -




![Image](https://github.com/user-attachments/assets/dfde76bd-dd2c-4e1a-ad64-c31caa397f3c)

Step-4

Now creating the target group-

navigate to services and search fro ec2 and drop down section will be target group -



![Image](https://github.com/user-attachments/assets/addac096-b71d-40fe-9831-c5324ad5027f)

We can see target group is created but not associated with load balancer so we are creating the load balancer-
We have created load lancer and new security group as load balance required internet access so we have allow on port 80



![Image](https://github.com/user-attachments/assets/137eb97c-aea5-4a9f-aa84-5bfab10257bc)

Step-5

When we go to create auto scaling group  it 'll ask what type of ec2 instance use so for that we need to ec2 launch template.
Here i'll  create a templete by Ec2 instance which have already running nginx server.

and created the auto scaling group as per below screen shot-

![Image](https://github.com/user-attachments/assets/c6596e73-42ae-46bc-b179-d906d2f1dba6)

Here we need to select the load balancer-

![Image](https://github.com/user-attachments/assets/354e05f2-e1fd-442d-aa8a-18b8ac3cb92b)

Next >



![Image](https://github.com/user-attachments/assets/c0f258fd-6162-4d5e-bd8e-19fd7b85a4c5)



Next >

Here we specified the what is the capacity min and desirer As i have kept min Min desired capacity is 1, adn max Max desired capacity is 3, and Desired capacity 2

![Image](https://github.com/user-attachments/assets/5cb41ba0-331f-4839-b24f-55c42abbcbb8)



![Image](https://github.com/user-attachments/assets/7ff0803f-f1e5-4462-b1a8-5b0e211db80b)



![Image](https://github.com/user-attachments/assets/ca7fc179-4d7d-4b2a-b3fe-6ff7f3b6f1ab)

Now auto scaling group created as per below image .since i have kept desired capacity 2 so it try to launch 2 ec2 instance .



![Image](https://github.com/user-attachments/assets/ed7d2a3f-2a65-40c9-b07f-0769eb48cc82)


What is Auto -scaling ?

AWS auto scaling monitor your applications and adjust capacity automatically to ensure consistent , predictable performance at the lowest possible cost . It is simple to set up application scaling for  multiple resource   across multiple services using aws auto scaling in minutes.


   

![Image](https://github.com/user-attachments/assets/03bf0ca1-f64d-43a8-8aa3-c60fdcbf0588)

* Scaling  is the process  of adding /removing capacity /resources as needed 
* Scale out is adding adding the capacity /resources
* scale in is removing the capacity /resource 

Types-

1- Vertical 
2- Horizontal



![Image](https://github.com/user-attachments/assets/acda89af-aa0a-4f03-9748-fcced02590b0)

Life cycle of Auto-Scaling:-



![Image](https://github.com/user-attachments/assets/111e18e1-1e4f-4a3f-b976-f373f56daf5f)


# What is Auto Scaling group ?

An auto scaling group contains a collection of Ec2 instance that exactly the same while creating an auto scaling group. The launch configuration must be specified after specified the launch configuration can not be change.
Ec2 instance are launched and terminated using scaling policy.






























































































Auto scaling component :- 

**Group**:

 Ec2 instance are in group so that they can be considered as a logical unit (for scaling and management)
When we create the group , we can  mention the following attributes:

The max, min , and desired number of instances. 

**Configuration templets**-: 

These are used as a configuration template for the ec2 instances .

Launch template or launch configuration is also used

**Scaling Option** 

Autoscaling provides several way to scale the group:

* manual scaling 
* Dynamic scaling 
* Scaling base on the demand or schedule 







