# What is S3 (Simple Storage Service ) ?

Amazon simple storage service (S3) is a storage that can be managed and access over the internet. S3 provide the web service that can be used to store retrieve unlimited amount of data . Same can be done programmatically using amazon provided APIs.

- It is resional service. regional service mean you need to select the region before starting it.

![Image](https://github.com/user-attachments/assets/bb1edb7f-cdc9-4c69-8830-8bed71539e5a)

Why company use S3 ?

1- S3 is cost effective storage service .This is also called object storage service . object storage mean you can store structured data and unstructured data 

What’s the Difference Between Structured Data and Unstructured Data?

tructured data and unstructured data are two broad categories of collectible data. [Structured data](https://aws.amazon.com/what-is/structured-data/) is data that fits neatly into data tables and includes discrete data types such as numbers, short text, and dates. Unstructured data doesn’t fit neatly into a data table because its size or nature: for example, audio and video files and large text documents. Sometimes, numerical or textual data can be unstructured because modeling it as a table is inefficient. For example, sensor data is a constant stream of numerical values, but creating a table with two columns—timestamp and sensor value—would be inefficient and impractical. Both structured data and unstructured data are essential in modern analytics.

**Bucket policy** - resource base policy 

Policy you are applying at aws service or resource level.
Bucket policy you can apply on the bucket level





#Some use full url for S3 bucket
- Finding the size of S3 buckets: https://aws.amazon.com/blogs/storage/find-out-the-size-of-your-amazon-s3-buckets/
- S3 Customer Stories: https://aws.amazon.com/s3/customers/
- Error reference for S3: https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html
- Use Cases of S3: https://aws.amazon.com/s3/
- Storage classes in S3: https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html
- S3 Pricing: https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html








You have been asked to:

1- Create S3 bucket to be Static website host and upload an index.html and error.html
2- Also, add a lifecycle rule for the bucket:
 a. Transition from Standard to Standard-IA in 60 days
  b. Expiration in 200 days


Step-1 Created the S3 bucket 

![Image](https://github.com/user-attachments/assets/53b40554-4d92-4dd9-9ab9-3eaf87b9211b)

Step-2 Created the index.html file ( Error page) for demo purpose 



![Image](https://github.com/user-attachments/assets/acc4ae13-2719-499b-b2f6-53714b31cba8)

Step-3

Created the index.html file for demo purpose 

![Image](https://github.com/user-attachments/assets/a02bb6d9-d1aa-4eac-9f00-d8e37cd1a8db)

Step-4

Uploaded the both file in S3 bucket 



![Image](https://github.com/user-attachments/assets/5debb853-f0a2-41b7-8312-624e256716c9)

Step-5 - Checking still not able to access the file.

![Image](https://github.com/user-attachments/assets/c7d35da6-9521-4610-b510-91ac84b73f7b)

Step-6

Unblocked public access

![Image](https://github.com/user-attachments/assets/62b8dcff-8c53-4cf6-9c55-eaff6fe6f738)

Step-7

Confirmed and saved

![Image](https://github.com/user-attachments/assets/1cf23456-5797-458f-8b9a-45533020f72b)

Step-8

clicked on ownership and enabled ACLS

![Image](https://github.com/user-attachments/assets/0c4e3f7c-fdca-4007-a24b-56a402889ef1)

Step-9

Make it public

![Image](https://github.com/user-attachments/assets/90dbc4c5-dcb5-4772-b26b-d6609ba36e88)

Step-10

After making public ,able to access the html error page and  index html  page also-

![Image](https://github.com/user-attachments/assets/5be47d36-8c07-466d-983d-c52b8ee28f40)

![Image](https://github.com/user-attachments/assets/8c4fd025-58ed-4e67-ab40-353c14777725)

Step-11

Life cycle rule created

![Image](https://github.com/user-attachments/assets/e3de0386-fb09-4eeb-a43c-5628f892089e)



# Hosting Static website on S3 Bucket using route 53

Step-1 Created the S3 bucket 

Here i have given the bucket name the name of my domain name which i have porched 



![Image](https://github.com/user-attachments/assets/52798236-766a-4314-bae0-34de3630487a)
![Image](https://github.com/user-attachments/assets/164b28bd-4217-4af3-baf6-13170fa64bf2)
![Image](https://github.com/user-attachments/assets/cbca2044-52be-43b5-ba28-cdc65e869488)
![Image](https://github.com/user-attachments/assets/3fa6d42f-9374-4d56-a50f-5d009aa91d52)

Step-2

I have created the 02 file and uploaded in bucket and made the both file public.
1- index.html
2- error.html
![Image](https://github.com/user-attachments/assets/ec8552dc-9538-454e-85aa-216c0c6a17a9)


Step-3

Go to the  bucket properties and enable the static website-

![Image](https://github.com/user-attachments/assets/28813059-b170-45bd-9aab-67003117bf4b)
![Image](https://github.com/user-attachments/assets/ee4db44b-e7c4-4c22-922a-f8e759eca323)
![Image](https://github.com/user-attachments/assets/f4d2f465-f6e7-40c6-9144-0625ad458acd)
![Image](https://github.com/user-attachments/assets/aced4e3f-fb04-4443-8044-95312b27a8bf)

Step-4

Now mention both file name(index.html and index.html) and saved

![Image](https://github.com/user-attachments/assets/1a3dde2c-1afe-4200-8356-951ff5739262)

Step-5

Now click on permission and edit  bucket policy and write code or  /copy policy from google like below  - 

![Image](https://github.com/user-attachments/assets/c60cb780-5f8b-41be-bc6f-09e8fe3bb753)

`
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::ajaycloud.shop/*"
            ]
        }
    ]
}

`
Step-5

Created the hosted zone and updated the name server record in my domain.

![Image](https://github.com/user-attachments/assets/ef2684fe-6256-46dd-aaae-06c3cf53fa4c)

Step-6

Create the record
![Image](https://github.com/user-attachments/assets/2f908a12-8f5b-4e79-a3f1-9d7be690f3bc)

Now my website is accessible by route 53

![Image](https://github.com/user-attachments/assets/9a3bcfa1-64ae-47ed-b836-8c03bbc990e4)



![Image](https://github.com/user-attachments/assets/882d59fb-4b6b-42a8-b020-a293df543d60)


Q1. What is hosted zone in Route 53?

 hosted zone when you want to use Route 53 to route internet traffic for your domain or to route traffic within your VPCs. Then you create records in the hosted zone for the domain name (example.com)

Q2. How internet traffic is routed to your website or web application ?

All computers on the internet, from your smart phone or laptop connect to the servers that serve content for massive retail websites, communicate with one another by using numbers. These numbers, known as IP addresses, are in one of the following formats:

Internet Protocol version 4 (IPv4) format, such as 192.0.2.44

Internet Protocol version 6 (IPv6) format, such as 2001:0db8:85a3:0000:0000:abcd:0001:2345

When you open a browser and go to a website, you don't have to remember and enter a long string of characters like that. Instead, you can enter a domain name like example.com and still end up in the right place. A DNS service such as Amazon Route 53 helps to make that connection between domain names and IP addresses.

### Overview of how you configure Amazon Route 53 to route internet traffic for your domain**

Here's an overview of how to use the Amazon Route 53 console to register a domain name and configure Route 53 to route internet traffic to your website or web application.

You register the domain name that you want your users to use to access your content. For an overview, see [How domain registration works](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-domain-registration.html).

After you register your domain name, Route 53 automatically creates a public hosted zone that has the same name as the domain. For more information, see [Working with public hosted zones](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/AboutHZWorkingWith.html).

To route traffic to your resources, you create records, also known as resource record sets, in your hosted zone. Each record includes information about how you want to route traffic for your domain, such as the following:

Name
The name of the record corresponds with the domain name (example.com) or subdomain name (www.example.com, retail.example.com) that you want Route 53 to route traffic for.

The name of every record in a hosted zone must end with the name of the hosted zone. For example, if the name of the hosted zone is example.com, all record names must end in example.com. The Route 53 console does this for you automatically.

Type
The record type usually determines the type of resource that you want traffic to be routed to. For example, to route traffic to an email server, you specify MX for Type. To route traffic to a web server that has an IPv4 IP address, you specify A for Type.

Value
Value is closely related to Type. If you specify MX for Type, you specify the names of one or more email servers for Value. If you specify A for Type, you specify an IP address in IPv4 format, such as 192.0.2.136.

For more information about records, see [Working with records](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/rrsets-working-with.html).

You can also create special Route 53 records, called alias records, that route traffic to Amazon S3 buckets, Amazon CloudFront distributions, and other AWS resources. For more information, see [Choosing between alias and non-alias records](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html) and [Routing internet traffic to your AWS resources](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-aws-resources.html).

For more information about routing internet traffic to your resources, see [Configuring Amazon Route 53 as your DNS service](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-configuring.html).

# How Amazon Route 53 routes traffic for your domain ?

After you configure Amazon Route 53 to route your internet traffic to your resources, such as web servers or Amazon S3 buckets, here's what happens in just a few milliseconds when someone requests content for www.example.com:

![Image](https://github.com/user-attachments/assets/c32fa947-517a-4465-a311-f4b5189246dc)

A user opens a web browser, enters www.example.com in the address bar, and presses Enter.

The request for www.example.com is routed to a DNS resolver, which is typically managed by the user's internet service provider (ISP), such as a cable internet provider, a DSL broadband provider, or a corporate network.

The DNS resolver for the ISP forwards the request for www.example.com to a DNS root name server.

The DNS resolver forwards the request for www.example.com again, this time to one of the TLD name servers for .com domains. The name server for .com domains responds to the request with the names of the four Route 53 name servers that are associated with the example.com domain.

The DNS resolver caches (stores) the four Route 53 name servers. The next time someone browses to example.com, the resolver skips steps 3 and 4 because it already has the name servers for example.com. The name servers are typically cached for two days.

The DNS resolver chooses a Route 53 name server and forwards the request for www.example.com to that name server.

The Route 53 name server looks in the example.com hosted zone for the www.example.com record, gets the associated value, such as the IP address for a web server, 192.0.2.44, and returns the IP address to the DNS resolver.

The DNS resolver finally has the IP address that the user needs. The resolver returns that value to the web browser.

Note
The DNS resolver also caches the IP address for example.com for an amount of time that you specify so that it can respond more quickly the next time someone browses to example.com. For more information, see [time to live (TTL)](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/route-53-concepts.html#route-53-concepts-time-to-live).

The web browser sends a request for www.example.com to the IP address that it got from the DNS resolver. This is where your content is, for example, a web server running on an Amazon EC2 instance or an Amazon S3 bucket that's configured as a website endpoint.

The web server or other resource at 192.0.2.44 returns the web page for www.example.com to the web browser, and the web browser displays the page.

### Working with public hosted zones

A public hosted zone is a container that holds information about how you want to route traffic on the internet for a specific domain, such as example.com, and its subdomains (acme.example.com, zenith.example.com). You get a public hosted zone in one of two ways:

When you register a domain with Route 53, we create a hosted zone for you automatically.

When you transfer DNS service for an existing domain to Route 53, you start by creating a hosted zone for the domain. For more information, see [Making Amazon Route 53 the DNS service for an existing domain](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/MigratingDNS.html).

In both cases, you then create records in the hosted zone to specify how you want to route traffic for the domain and subdomains. For example, you might create a record to route traffic for www.example.com to a CloudFront distribution or to a web server in your data center. For more information about records, see [Working with records](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/rrsets-working-with.html).


### Working with private hosted zones

A private hosted zone is a container that holds information about how you want Amazon Route 53 to respond to DNS queries for a domain and its subdomains within one or more VPCs that you create with the Amazon VPC service. Here's how private hosted zones work:

You create a private hosted zone, such as example.com, and specify the VPC that you want to associate with the hosted zone. After you create the hosted zone you can associate more VPCs with it.

You create records in the hosted zone that determine how Route 53 responds to DNS queries for your domain and subdomains within and among your VPCs. For example, suppose you have a database server that runs on an EC2 instance in the VPC that you associated with your private hosted zone. You create an A or AAAA record, such as db.example.com, and you specify the IP address of the database server.

For more information about records, see [Working with records](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/rrsets-working-with.html). For information about the Amazon VPC requirements for using private hosted zones, see [Using private hosted zones](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-dns.html#vpc-private-hosted-zones) in the Amazon VPC User Guide.

When an application submits a DNS query for db.example.com, Route 53 returns the corresponding IP address. To get an answer from a private hosted zone you also have to be running an EC2 instance in one of the associated VPCs (or have an inbound endpoint from a hybrid setup.) If you try to query a private hosted zone from outside the VPCs or your hybrid setup, the query will be recursively resolved on the internet.

The application uses the IP address that it got from Route 53 to establish a connection with the database server.

When you create a private hosted zone, the following name servers are used:

ns-0.awsdns-00.com

ns-512.awsdns-00.net

ns-1024.awsdns-00.org

ns-1536.awsdns-00.co.uk

These name servers are used because the DNS protocol requires that every hosted zone must have an NS record set. These name servers are reserved and never used by Route 53 public hosted zones. You can only query those zones via Route 53 Resolver in a VPC that has been associated to the hosted zone by using an inbound endpoint connected to the VPCs specified in the private hosted zone.

While the name servers are visible on the internet, Route 53 Resolver doesn't connect to the name server addresses. Further, the private hosted zone information is not returned if you directly query the name servers over the internet. Instead, the Route 53 Resolver detects that queries are within a private namespace based on VPC to hosted zone associations and uses direct, private connectivity to reach the private DNS servers.

Note
You can change the NS record set in a private hosted zone if you want and private DNS resolution will still work. We don't recommend doing so, but if you choose to, you should use reserved domain names which are not used by public DNS servers.

If you want to route traffic for your domain on the internet, you use a Route 53 public hosted zone. For more information, see [Working with public hosted zones](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/AboutHZWorkingWith.html).

