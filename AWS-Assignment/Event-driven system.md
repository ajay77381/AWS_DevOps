What is Event-driven system ?

An [event-driven architecture](https://aws.amazon.com/event-driven-architecture/) uses messages, or events, to trigger and communicate between decoupled services and is common in modern applications built with microservices. Events contain information about a change in a system’s state, such as a new order or a completed payment. Focusing on events helps avoid tight-coupling and can promote greater flexibility and extensibility for applications, which in turn helps improve feature velocity and agility for your developer teams.You can visit the [serverless product page](https://aws.amazon.com/serverless/) to learn more.


## What is the decoupled system?

Decoupled, or decoupling, is a state of an IT environment in which two or more systems somehow work or are connected without being directly connected.


# Benefits of an event-driven architecture

### Scale and fail independently:

By decoupling your services, they are only aware of the event router, not each other. This means that your services are interoperable, but if one service has a failure, the rest will keep running. The event router acts as an elastic buffer that will accommodate surges in workloads.

###  Develop with agility-

You no longer need to write custom code to poll, filter, and route events; the event router will automatically filter and push events to consumers. The router also removes the need for heavy coordination between producer and consumer services, speeding up your development process.

### Audit with ease

An event router acts as a centralized location to audit your application and define policies. These policies can restrict who can publish and subscribe to a router and control which users and resources have permission to access your data. You can also encrypt your events both in transit and at rest.

### Cut costs

Event-driven architectures are push-based, so everything happens on-demand as the event presents itself in the router. This way, you’re not paying for continuous polling to check for an event. This means less network bandwidth consumption, less CPU utilization, less idle fleet capacity, and less SSL/TLS handshakes


# How it works: example architecture ?

Here's an example of an event-driven architecture for an e-commerce site. This architecture enables the site to react to changes from a variety of sources during times of peak demand, without crashing the application or over-provisioning resources.




![Image](https://github.com/user-attachments/assets/5c3edafd-f237-4fbf-b3b0-c9b7ed48935f)






## When to use this architecture ?

- Cross-account, cross-region data replication

You can use an event-driven architecture to coordinate systems between teams operating in and deploying across different regions and accounts. By using an event router to transfer data between systems, you can develop, scale, and deploy services independently from other teams.

- Resource state monitoring and alerting

Rather than continuously checking on your resources, you can use an event-driven architecture to monitor and receive alerts on any anomalies, changes, and updates. These resources can include storage buckets, database tables, serverless functions, compute nodes, and more.

- Fanout and parallel processing

If you have a lot of systems that need to operate in response to an event, you can use an event-driven architecture to fanout the event without having to write custom code to push to each consumer. The router will push the event to the systems, each of which can process the event in parallel with a different purpose.


- Integration of heterogeneous systems

If you have systems running on different stacks, you can use an event-driven architecture to share information between them without coupling. The event router establishes indirection and interoperability among the systems, so they can exchange messages and data while remaining agnostic.


## Should you use an event-driven architecture?

Event-driven architectures are ideal for improving agility and moving quickly. They’re commonly found in modern applications that use microservices, or any application that has decoupled components. When adopting an event-driven architecture, you may need to rethink the way you view your application design. To set yourself up for success, consider the following:

• The durability of your event source. Your event source should be reliable and guarantee delivery if you need to process every single event. 

• Your performance control requirements. Your application should be able to handle the asynchronous nature of event routers. 

• Your event flow tracking. The indirection introduced by an event-driven architecture allows for dynamic tracking via monitoring services, but not static tracking via code analysis. 

• The data in your event source. If you need to rebuild state, your event source should be deduplicated and ordered.

[Download the AWS Event-Driven Architecture guide »](https://pages.awscloud.com/global-ln-gc-300-building-eda-on-aws-guide-learn.html)



## Where to start

There are two main types of routers used in event-driven architectures: event buses and event topics. At AWS, we offer [Amazon EventBridge](https://aws.amazon.com/eventbridge/) to build event buses and [Amazon Simple Notification Service (SNS)](https://aws.amazon.com/sns/) to build event topics.

**Amazon EventBridge** is recommended when you want to build an application that reacts to events from SaaS applications, AWS services, or custom applications. EventBridge uses a predefined schema for events and allows you to create rules that are applied across the entire event body to filter before pushing to consumers.

[Create your first event bus with this tutorial »](https://pages.awscloud.com/AWS-Learning-Path-How-to-Use-Amazon-EventBridge-to-Build-Decoupled-Event-Driven-Architectures_2020_LP_0001-SRV.html?&trk=ps_a134p000003yBd8AAE&trkCampaign=FY20_2Q_eventbridge_learning_path&sc_channel=ps&sc_campaign=FY20_2Q_EDAPage_eventbridge_learning_path&sc_outcome=PaaS_Digital_Marketing&sc_publisher=Google)
[Dive deeper on EventBridge with this webinar »](https://pages.awscloud.com/Deep-Dive-on-Amazon-EventBridge_2019_0919-SRV_OD.html)

**Amazon SNS** is recommended when you want to build an application that reacts to high throughput and low latency events published by other applications, microservices, or AWS services, or for applications that need very high fanout (thousands or millions of endpoints). SNS topics are agnostic to the event schema coming through.
[Send fanout event notifications with this tutorial »](https://aws.amazon.com/getting-started/tutorials/send-fanout-event-notifications/)
[Read this blog on building Event-Driven Architectures »](https://aws.amazon.com/blogs/compute/enriching-event-driven-architectures-with-aws-event-fork-pipelines/)


























