Reference URL- https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html



# What is Amazon CloudWatch?

AWS CloudWatch is a powerful monitoring and observability service provided by Amazon Web Services. CloudWatch collects and tracks metrics, collects and monitors log files, and sets alarms to alert you on certain conditions.

# Advantages of AWS CloudWatch:

**Comprehensive Monitoring**: CloudWatch allows you to monitor various AWS resources such as EC2 instances, RDS databases, Lambda functions, and more. You get a unified view of your entire AWS infrastructure.

**Real-Time Metrics**: It provides real-time monitoring of metrics, allowing you to respond quickly to any issues or anomalies that might arise.

**Automated Actions**: With CloudWatch Alarms, you can set up automated actions like triggering an Auto Scaling group to scale in or out based on certain conditions.

**Log Insights**: CloudWatch Insights lets you analyze and search log data from various AWS services, making it easier to troubleshoot problems and identify trends.

Dashboards and Visualization: Create custom dashboards to visualize your application and infrastructure metrics in one place, making it easier to understand the overall health of your system.

# Problem Solving with AWS CloudWatch:

CloudWatch helps address several critical challenges, including:

Resource Utilization: Tracking resource utilization and performance metrics to optimize your AWS infrastructure efficiently.
Proactive Monitoring: Identifying and resolving issues before they impact your applications or users.
Troubleshooting: Analyzing logs and metrics to troubleshoot problems and reduce downtime.
Scalability: Automatically scaling resources based on demand to ensure optimal performance and cost efficiency.

# Practical Use Cases of AWS CloudWatch:

Auto Scaling: CloudWatch can trigger Auto Scaling actions based on defined thresholds. For example, you can automatically scale in or out based on CPU utilization or request counts.

Resource Monitoring: Monitor EC2 instances, RDS databases, DynamoDB tables, and other AWS resources to gain insights into their performance and health.

Application Insights: Track application-specific metrics to monitor the performance of your applications and identify potential bottlenecks.

Log Analysis: Use CloudWatch Logs Insights to analyze log data, identify patterns, and troubleshoot issues in real-time.

Billing and Cost Monitoring: CloudWatch can help you monitor your AWS billing and usage patterns, enabling you to optimize costs.

## Accessing CloudWatch

You can access CloudWatch using any of the following methods:

Amazon CloudWatch console – https://console.aws.amazon.com/cloudwatch/

AWS CLI – For more information, see [Getting Set Up with the AWS Command Line Interface](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-set-up.html) in the AWS Command Line Interface User Guide.

CloudWatch API – For more information, see the [Amazon CloudWatch API Reference](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/Welcome.html).

AWS SDKs – For more information, see [Tools for Amazon Web Services](http://aws.amazon.com/tools).


Related AWS services:

The following services are used along with Amazon CloudWatch:

-Amazon Simple Notification Service (Amazon SNS) coordinates and manages the delivery or sending of messages to subscribing endpoints or clients. You use Amazon SNS with CloudWatch to send messages when an alarm threshold has been reached. For more information, see [Setting up Amazon SNS notifications](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Notify_Users_Alarm_Changes.html#US_SetupSNS).

- Amazon EC2 Auto Scaling enables you to automatically launch or terminate Amazon EC2 instances based on user-defined policies, health status checks, and schedules. You can use a CloudWatch alarm with Amazon EC2 Auto Scaling to scale your EC2 instances based on demand. For more information, see [Dynamic Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) in the Amazon EC2 Auto Scaling User Guide.

- AWS CloudTrail enables you to monitor the calls made to the Amazon CloudWatch API for your account, including calls made by the AWS Management Console, AWS CLI, and other services. When CloudTrail logging is turned on, CloudWatch writes log files to the Amazon S3 bucket that you specified when you configured CloudTrail. For more information, see [Logging Amazon CloudWatch API and console operations with AWS CloudTrail](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/logging_cw_api_calls.html).

- AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources for your users. Use IAM to control who can use your AWS resources (authentication) and what resources they can use in which ways (authorization). For more information, see [Identity and access management for Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/auth-and-access-control-cw.html).


Billing and costs-

For complete information about CloudWatch pricing, see [Amazon CloudWatch Pricing](https://aws.amazon.com/cloudwatch/pricing/).

For information that can help you analyze your bill and possibly optimize and reduce costs, see [CloudWatch billing and cost](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_billing.html).


# How Amazon CloudWatch works

Amazon CloudWatch is basically a metrics repository. An AWS service—such as Amazon EC2—puts metrics into the repository, and you retrieve statistics based on those metrics. If you put your own custom metrics into the repository, you can retrieve statistics on these metrics as well.

You can use metrics to calculate statistics and then present the data graphically in the CloudWatch console. For more information about the other AWS resources that generate and send metrics to CloudWatch, see [AWS services that publish CloudWatch metrics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html).

You can configure alarm actions to stop, start, or terminate an Amazon EC2 instance when certain criteria are met. In addition, you can create alarms that initiate Amazon EC2 Auto Scaling and Amazon Simple Notification Service (Amazon SNS) actions on your behalf. For more information about creating CloudWatch alarms, see [Alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#CloudWatchAlarms).

AWS Cloud computing resources are housed in highly available data center facilities. To provide additional scalability and reliability, each data center facility is located in a specific geographical area, known as a Region. Each Region is designed to be completely isolated from the other Regions, to achieve the greatest possible failure isolation and stability. Metrics are stored separately in Regions, but you can use CloudWatch cross-Region functionality to aggregate statistics from different Regions. For more information, see [Cross-account cross-Region CloudWatch console](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Cross-Account-Cross-Region.html) and [Regions and Endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#cw_region) in the Amazon Web Services General Reference.




Created EC2-



![Image](https://github.com/user-attachments/assets/73cb287c-fa8b-47f5-b10c-81ad97456f19)

After log in on Ec2 instance and created a file (cpu_spike.py)  for run and increase the CPU utilization -



![Image](https://github.com/user-attachments/assets/d48f3527-468d-4ab6-a1da-e20e2602d8a3)

Now CPU Spike file is running -



![Image](https://github.com/user-attachments/assets/7fc0127b-9abb-4259-b87b-b19e75e9ed65)

And we can see in cloudwatch CPU utilization is-



![Image](https://github.com/user-attachments/assets/6dd5a75c-9078-40c3-8d69-a6aac4228d54)

Now we can see maximum CPU utilization is above 50 %



![Image](https://github.com/user-attachments/assets/f97f633a-e6a8-447e-b955-73827d7ce920)

Note- with matrix we collect all the information about CPU utilization and memory utilization and api related information.

Created  the Alarm in cloudwatch as per below image-


![Image](https://github.com/user-attachments/assets/1e24e526-eb13-47f7-a1dd-4ff2b7ff9d8a)



![Image](https://github.com/user-attachments/assets/0bdffa5d-1224-4dd3-97cc-5de08de89b26)


Now Alarm is created -


![Image](https://github.com/user-attachments/assets/e3f8e301-a1d8-4f90-9d1f-29bda8e712de)

For activating the alarm we need to open the email and approve the email send by amazon sns  as per below-



![Image](https://github.com/user-attachments/assets/e1bc59b5-c82b-46e4-b81a-0830dc404675)

Now we can see alarm is activated-



![Image](https://github.com/user-attachments/assets/3d9abad2-82cd-4146-9700-aa5fe8d46f42)

When ever CPU utilization will be more  than %50% we'll receive a alert on my email- 

Now we can see CPU utilization reached at 50% as per below -


![Image](https://github.com/user-attachments/assets/e1dbfe9a-d067-42d0-b2b7-23c18f3211b4)


I have received the alert on my email ID-  ajay77381@gmail.com



![Image](https://github.com/user-attachments/assets/291ec208-141b-48e8-a426-d1bfaecabc62)



Q-1- What is different between CloudWatch and Cloud Trail ?

**CloudTrail**
Records all API activity and management events in an AWS account, including who made a request, the services used, and the actions performed. It's useful for auditing and compliance purposes, as well as forensic analysis, troubleshooting, and incident management. CloudTrail logs are saved on S3 and can be analyzed using a service like Athena. CloudTrail is enabled by default when you create an AWS account, and a single trial that offers a single copy of management events in every area is free.
**CloudWatch**
Provides real-time monitoring and operational management capabilities for AWS resources and applications. It can collect metrics and logs from AWS or on-prem resources, apps, and services, and provide visualizations of apps and infrastructure in dashboards. CloudWatch can also alert you when certain metrics require attention, and help you find opportunities for optimization and cost reduction. For example, you can specify what happens when a specific threshold is met, such as terminating an EC2 instance if a condition is met, or creating additional instances to support more traffic. CloudWatch offers free basic monitoring for resources like EC2 instances, EBS volumes, and RDS DB instances.  


















