IP classes-

Private IP address-

Class A- 10.0.0.0 to 10.255.255.255

Class B- 172.16.0.0 to 172.31.255.255

Class C- 198.168.0.0 to 192.168.255.255

Class D & E reserved for multicalst and sciencetistific purpose.

1 byte = 8 bit




![image](https://github.com/user-attachments/assets/05aadebd-b6aa-417c-b7f5-1644a7f09c32)

As per above why we are writing -5 and why not -2 like CCNA subneting.

Because as per microsoft azure we can not use the below ip address because these ip address are resereved for specfic purpose.

10.0.0.0
10.0.0.1
10.0.0.2
10.0.0.3
10.255.255.255 - Broad cost IP 

**Note- for azure peospective we user formula 2^n-5**
but in general termenology we user 2^n-2

Example- VNET

![image](https://github.com/user-attachments/assets/1d115f95-daea-49d3-8720-59652ce80c3f)

What is Azure Virtual netowrk ?

Azure virtual network )VNET) is the fundamental building block for your private network in Azure. Vnet enable many type of azure resource such as Azure virutal machine (VM) to securly communicate each other, the internet and on premises network. 

## VNET component 

1- Address space 
2- Subnet 
3- Region 
4- Subscription

- An address space is the range of ip address . Azure will assign the next available ip address from this address space to resource in your virutal netwok.
  Like- 10.0.0.0\24
  
- Subnet is the logical segment of a virutal network . A subnet is allocated a portion of the virtual network address's space.
- Region - virtual networks are scoped to a single single location called a region . Multiple virtual network from diffrent regions can be connected together using virtual network peering.
- Subscription- virtual network are scoped to a subscription. You can impliment multiple virtual network within each azure subscription and azure region.

  ## What is Azure extended zone ?

  Azure extended zone are an offering from microsoft azure that enable data processing close to user. You can deploy VMs,containers, storage, and other azure service into Azure extended zones to address the low latency and high throughput requirement of application .

  Azure extended is a premimum solution for azure and will incure aditional charges.

  ## What is Azure Bastion ?

  Azure bastion is the service that provide secure RDP / SSh connectivity to your virtual machine over TLS when you connect via Azure Bastion , you virtual machine do not need a public address and you would be able to access the machine by browser also.

  ![image](https://github.com/user-attachments/assets/c9988959-a176-4aad-aaea-2ff55d188e86)


  Azure Firewall - is a manage cloud base network security service that protect your Azure virtual network resource.
  

Created one Vnet -Example

![image](https://github.com/user-attachments/assets/330cb227-8d80-4167-ba52-697567242133)

What is diffrent between address space and subnet ?

What ever CIDR notastion we provide on VPC level that is address space and what ever cidr notation we give for subnet level that is subnet address range.


# Connecting diffrent VNET or vnet peering ?

Peering the the connection of multiple vnets and there is two type of peering 

1- Regional peering 

2- Global peering

What is REgional peering - Wehen you connect two network in same region that is called Regional peering.

whtat is global peering - when you connect two network in diffrent region that is called global peering.


## There are two way you can connect your azure vnets.

1- Vnet peering 

2- Vnet to Vnet connection gateway

Note- when two vnet connected together they are on the microsoft backbone network . It means those are on the private network

Vnet peering-

Step

01 - Created  two VPC and launched 01 virtual machine in each VPC subnet and enabled the peering in both VPC and we are able to ping and take remote by private ip address.

![image](https://github.com/user-attachments/assets/31ed3588-47a8-4acf-beee-5a829b2f6044)

Enabled the Peering-

![image](https://github.com/user-attachments/assets/efbed449-4133-4b10-9086-6836cb0c9a95)



#####################################################################

# Connect two Vnet each other using VNet to Vnet VPN gateway connection. This connection type use a VPN gateway to provide a secure tunnel with IP sec /IkE and function the same way communication.


![image](https://github.com/user-attachments/assets/666e3f27-cc49-4aa9-a194-0f91d8597b6b)


Step

1- 

![image](https://github.com/user-attachments/assets/703c35d4-b96e-4188-8a8f-d49d1e119e60)


* Note- VGN gateway required seprate gatway subnet then it 'll work


####################################################################################


# How to connect your On-Premise network to Azure virtual network ?

There are three way to connect your On-Premise network to azure virtual network

1- P2s ( Point to site connection) - When you connectiong your laptop from on primise to cloud VPC
2- S2S ( Site to site connection) - That is yor onprime office and that is connected to Azure Cloud netowrk 
3- Express route (Dedicated  line) - Dedicated fiber line from your on premise network to Azure Cloud network



### How to assign a static ip address to a virutal machine ?





