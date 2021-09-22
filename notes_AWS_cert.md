## AWS Cloud Practitioner Essentials
https://www.aws.training/Details/eLearning?id=60697


### Module 1. Intro
#### Objectives
- Summarize the benefits of AWS.
- Describe differences between on-demand delivery and cloud deployments.
- Summarize the pay-as-you-go pricing model.
#### notes
1. client-server model
In computing, a client can be a web browser or desktop application that a person interacts with to make requests to computer servers. A server can be services such as Amazon Elastic Compute Cloud (Amazon EC2), a type of virtual server.
For example, suppose that a client makes a request for a news article, the score in an online game, or a funny video. The server evaluates the details of this request and fulfills it by returning the information to the client.

2. Cloud computing is the **on-demand delivery of IT resources and applications over the internet with pay-as-you-go pricing**.
- on-demand delivery
AWS has the resources you need, when you need them.
- undifferentiated heavy lifting of IT
AWS helps with tasks that are common, often repetitive and ultimately time-consuming. 
- over the internet
you can access those resources using a secure webpage console or programmatically. 
- pay for what you need

3. Deployment models for cloud computing
1) cloud-based deployment
- Run all parts of the application in the cloud.
You can build applications on low-level infrastructure that requires your IT staff to manage them. Alternatively, you can build them using higher-level services that reduce the management, architecting, and scaling requirements of the core infrastructure. 
For example, a company might create an application consisting of virtual servers, databases, and networking components that are fully based in the cloud.
- Migrate existing applications to the cloud.
- Design and build new applications in the cloud.

2) on-premises deployment
On-premises deployment is also known as a **private cloud deployment**. 
- Deploy resources by using virtualization and resource management tools.
- Increase resource utilization by using application management and virtualization technologies.
For example, you might have applications that run on technology that is fully kept in your on-premises data center. Though this model is much like legacy IT infrastructure, its incorporation of application management and virtualization technologies helps to increase resource utilization.

3) hybrid deployment
- Connect cloud-based resources to on-premises infrastructure.
For example, you have legacy applications that are better maintained on premises, or government regulations require your business to keep certain records on premises.
- Integrate cloud-based resources with legacy IT applications.
For example, suppose that a company wants to use cloud services that can automate batch data processing and analytics. However, the company has several legacy applications that are more suitable on premises and will not be migrated to the cloud. With a hybrid deployment, the company would be able to keep the legacy applications on premises while benefiting from the data and analytics services that run in the cloud.

4. Benefits of cloud computing
- trade upfront expense for variable expense
Upfront expense refers to data centers, physical servers, and other resources that you would need to invest in before using them. Variable expense means you only pay for computing resources you consume instead of investing heavily in data centers and servers before you know how you’re going to use them.
By taking a cloud computing approach that offers the benefit of variable expense, companies can implement innovative solutions while saving on costs of investment in technology resources. 

- stop spending money to run and maintain data centers
Computing in data centers often requires you to spend more money and time managing infrastructure and servers. 
A benefit of cloud computing is the ability to focus less on these tasks and more on your applications and customers.

- stop guessing capacity
With cloud computing, you don’t have to predict how much infrastructure capacity you will need before deploying an application. 
For example, you can launch Amazon EC2 instances when needed, and pay only for the compute time you use. Instead of **accessing services on-demand to prevent excess or limited capacity**, you can access only the capacity that you need. You can also scale in or scale out in response to demand.

- benefit from massive economies of scale
**The aggregated cloud usage from a large number of customers in the cloud providers, such as AWS, results in lower pay-as-you-go prices.** 

- increase speed and agility
The flexibility of cloud computing makes it easier for you to develop and deploy applications.
This flexibility provides you with more time to experiment and innovate. When computing in data centers, it may take weeks to obtain new resources that you need. By comparison, cloud computing enables you to access new resources within minutes.

- go global in minutes
The global footprint of the AWS Cloud enables you to **deploy applications to customers around the world quickly with low latency**. This means that even if you are located in a different part of the world than your customers, customers are able to access your applications with minimal delays. 

5. References

[AWS glossary](https://docs.aws.amazon.com/general/latest/gr/glos-chap.html)
[Whitepaper: Overview of Amazon Web Services](https://d0.awsstatic.com/whitepapers/aws-overview.pdf)
[AWS Fundamentals: Overview](https://aws.amazon.com/getting-started/fundamentals-overview/)
[What is cloud computing?](https://aws.amazon.com/what-is-cloud-computing/)
[Types of cloud computing](https://aws.amazon.com/types-of-cloud-computing/)
[Cloud computing with AWS](https://aws.amazon.com/what-is-aws/)


### Module 2. Compute in the Cloud
#### Objectives
- Describe the benefits of Amazon Elastic Compute Cloud (Amazon EC2) at a basic level
- Identify the different Amazon EC2 instance types
- Differentiate between the various billing options for Amazon EC2
- Describe the benefits of Amazon EC2 Auto Scaling
- Summarize the benefits of Elastic Load Balancing
- Give an example of the uses for Elastic Load Balancing
- Summarize the differences between Amazon Simple Notification Service (Amazon SNS) and Amazon Simple Queue Services (Amazon SQS)
- Summarize additional AWS compute options
#### notes
1. Ease of provisioning EC2 instances
- Elastic Compute Cloud (EC2)
EC2 provides secure, resizable compute capacity in the cloud as Amazon EC2 instances. 
- Compute as a Service (CaaS) model 
- instances, also know as virtual machines

2. Comparison over websites' architecture
1) traditional on-premises resources
- spend money upfront to purchase hardware
- wait for the servers to be delivered
- install the servers in physical data center
- make all the necessary configurations

2) EC2 instance 
use a virtual server to run applications in the AWS cloud
- provision and launch an Amazon EC2 instance within minutes
- spin up new servers or take them offline at will
stop using it when having finished running a workload
- only pay for compute time when an instance is running, not stopped or terminated instances
- only pay for server capacity needed

3. Multitenancy
- EC2 runs on top of physical host machines managed by AWS using virtualization technology. When you spin up an EC2 instance, you aren't necessarily taking an entire host to yourself. Instead, you are sharing the host with multiple other instances. 
- A hypervisor running on the host machine is responsible for sharing the underlying physical resources between the instances/virtual machines. This idea of sharing underlying hardware is called multitenancy.
- The hypervisor is responsible for coordinating this multitenancy and it is managed by AWS. 
- The hypervisor is responsible for isolating the virtual machines from each other as they share resources from the host. This means EC2 instances are secure. Even though they may be sharing resources, one EC2 instance is not aware of any other EC2 instances also on that host. They are secure and separate from each other. 

4. EC2's flexibility and control over instances configuration
- operating system 
When you provision an EC2 instance, you can choose the operating system based on either Windows or Linux. You can provision thousands of EC2 instances on demand. With a blend of operating systems and configurations to power your business' different applications. 
- software 
internal business aspps, web apps, databases, 3rd-party software like enterprise software packages.
- resizable instances/vertical scaling
You might start with a small instance, realize the application you are running is starting to max out that server, and then you can give that instance more memory and more CPU. Which is what we call vertically scaling an instance. 
- networking
what type of requests make it to your server, if they are publicly or privately accessible. 

5. How EC2 works
1) launch an instance
- select a template w/ basic configs for instance
These configs include the hardware, os, application server, applications.
- specify security settings to control the network traffic that can flow into and out of instance

2) connect
You can connect to instance in several ways
- programs and applications have multiple dft methods to connect directly to the instance and exchange data
- users can also connect to instance by logging in and accessing the computer desktop

3) use
After having connected to the instnace, begin using it
- run commands to install software, add storage, copy and organize files, etc

6. instance types
1) EC2 instance families
Each EC2 instance type is grouped under an instance family, and are optimized for certain types of tasks. Instance types offer varying combinations of CPU, memory, storage, and network capacity, and give you the flexibility to choose the appropriate mix of resources for your applications.

A. general purpose
- **balanced resources of compute, memory, and networking**
- diverse workloads like: web service, application servers, gaming servers, backend servers for enterprise applications, code repositories, small and medium databases.
Suppose that you have an application in which the resource needs for compute, memory, and networking are roughly equivalent. You might consider running it on a general purpose instance because the application does not require optimization in any single resource area.

B. **compute optimized**
- compute-bound applications that benefit from **high-performance processors**
- gaming servers, high performance computing (HPC), scientific modeling.
Like general purpose instances, you can use compute optimized instances for workloads such as web, application, and gaming servers.
The difference is compute optimized applications are ideal for high-performance web servers, compute-intensive applications servers, and dedicated gaming servers. 
You can also use compute optimized instances for **batch processing workloads that require processing many transactions in a single group**.

C. accelerated computing
- task utilizing hardware accelerators
Accelerated computing instances use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs. 
In computing, a hardware accelerator is a component that can expedite data processing. 
- floating point number calculations, graphics processing, data pattern matching
Accelerated computing instances are ideal for workloads such as graphics applications, game streaming, and application streaming.

D. **memory optimized**
- good for memory-intensive task, **ideal for workloads that process large datasets in memory, such as high-performance databases**
Memory optimized instances are designed to deliver fast performance for workloads with high memory needs. 
In computing, memory is a temporary storage area. It holds all the data and instructions that a central processing unit (CPU) needs to be able to complete actions. Before a computer program or application is able to run, it is loaded from storage into memory. This preloading process gives the CPU direct access to the computer program.
Suppose that you have a workload that requires large amounts of data to be preloaded before running an application. 
- This scenario might be a high-performance database or a workload that involves performing real-time processing of a large amount of unstructured data. In these types of use cases, consider using a memory optimized instance. 

E. **storage optimized**
- workloads requiring **high, sequential read and write access to large datasets on local storage** & **suitable for data warehousing applications**
Storage optimized instances are designed for workloads that require high, sequential read and write access to large datasets on local storage. Examples of workloads suitable for storage optimized instances include distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems.
In computing, the term input/output operations per second (IOPS) is a metric that measures the performance of a storage device. It indicates how many different input or output operations a device can perform in one second. Storage optimized instances are designed to deliver tens of thousands of low-latency, random IOPS to applications. 
You can think of input operations as data put into a system, such as records entered into a database. An output operation is data generated by a server. 
- An example of output might be the analytics performed on the records in a database
If you have an application that has a high IOPS requirement, a storage optimized instance can provide better performance over other instance types not optimized for this kind of use case.

2) References

[EC2 instance types](https://aws.amazon.com/ec2/instance-types/)

7. EC2 pricing
1) **on-demand**
- **most flexible, no contract/upfront costs**. The instances run continuously until you stop them, and you pay for only the compute time you use.
- short-term, irregular workloads that cannot be interrupted. 
Sample use cases for On-Demand Instances include developing and testing applications and running applications that have unpredictable usage patterns. On-Demand Instances are not recommended for workloads that last a year or longer because these workloads can experience greater cost savings using Reserved Instances.

2) **spot instances**
- **allows you to utilize unused capacity at a discounted rate**. 
- unlike savings plans, spot instances **do not require contracts or a commitment to a consistent amount of compute usage**. 
- ideal for workloads with **flexible start and end times, or that can withstand interruptions**. 
Suppose that you have a background processing job that can start and stop as needed (such as the data processing job for a customer survey). You want to start and stop the processing job without affecting the overall operations of your business. If you make a Spot request and Amazon EC2 capacity is available, your Spot Instance launches. However, if you make a Spot request and Amazon EC2 capacity is unavailable, the request is not successful until capacity becomes available. The unavailable capacity might delay the launch of your background processing job. After you have launched a Spot Instance, if capacity is no longer available or demand for Spot Instances increases, your instance may be interrupted. This might not pose any issues for your background processing job. However, in the earlier example of developing and testing applications, you would most likely want to avoid unexpected interruptions. Therefore, choose a different EC2 instance type that is ideal for those tasks.

3) savings plans
- **contract w/ discounted rate for a commit to certain level of usage**
ideal for workloads involving **a consistent amount of compute usage over a 1-year or 3-year term**. This term commitment results in savings of up to 72% over On-Demand costs.
- Any usage up to the commitment is charged at the discounted plan rate (for example, $10 an hour). Any usage beyond the commitment is charged at regular On-Demand rates.

4) reserved instances
- **contract w/ discounted rate for a commit to certain level of usage**
You can purchase Standard Reserved and Convertible Reserved Instances for a 1-year or 3-year term, and Scheduled Reserved Instances for a 1-year term. You realize greater cost savings with the 3-year option.
- At the end of a Reserved Instance term, you can continue using the Amazon EC2 instance without interruption. However, you are charged On-Demand rates until you do one of the following:
A. Terminate the instance.
B. Purchase a new Reserved Instance that matches the instance attributes (instance type, Region, tenancy, and platform).

5) dedicated hosts
- Dedicated Hosts are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. 
- You can use your existing per-socket, per-core, or per-VM software licenses to help maintain license compliance. You can purchase On-Demand Dedicated Hosts and Dedicated Hosts Reservations. Of all the Amazon EC2 options that were covered, Dedicated Hosts are the most expensive.

8. Scaling Amazon EC2
1) Scalability
- Scalability involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. 
- As a result, you pay for only the resources you use. You don’t have to worry about a lack of computing capacity to meet your customers’ needs.
- scaling
You can sale EC2 instances either **vertically by resizing the instance**, or **horizontally by launching new instances and adding them to the pool**. 

2) **EC2 Auto Scaling** 
- automated horizontal scaling
cost-effective architecture enabling you to **automatically add/remove Amazon EC2 instances in response to changing application demand**, maintaining a greater sense of application availability. 
- two approaches
A. dynamic scaling: responds to changing demand
B. predictive scaling: automatically schedules the right number of Amazon EC2 instances based on predicted demand
To scale faster, you can use dynamic scaling and predictive scaling together
- configurations when creating an Auto Scaling group
A. minimum capacity: the number of Amazon EC2 instances that launch immediately after you have created the Auto Scaling group.
B. desired capacity: you can set the desired capacity at two Amazon EC2 instances even though your application needs a minimum of a single Amazon EC2 instance to run.
C. maximum capacity: btw desired and maximum, it is scale as needed. 

9. Directing traffic w/ Elastic Load Balancing
1) Load Balancer
A load balancer is an application that takes in requests and routes them to the instances to be processed. 
It's a single point of contact for all incoming web traffic to Auto Scaling group. This means as you add/remove EC2 instances in response to the amount of incoming traffic, these requests route to the load balancer first. Then the requests spread across multiple resources that will handle them. 

2) **ELB** can properly distribute traffic
ELB is an AWS service that automates load balancing. It **automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances**.
[ELB low-demand](./img/ELB_low_demand.png) vs [ELB high demand](./img/ELB_high_demand.png)
- high performance
- cost-efficient
- highly available 
ELB is a regional construct (runs at the regional level rather than on individual EC2 instances) so it can be highly available automatically without additional effort on your part. 
ELB also solves the internal communication between front and back end through a decoupled architecture: because it's regional, it is a single URL that each front end instance uses. The ELB directs traffic to the back end that has the least outstanding requests. If the back end scales, it will inform the ELB that it can take more traffic once the new instances are ready, without having front end bothering about the details. 
- automatically scalable
As the traffic grows, ELB is designed to handle the additional throughput with no change to the hourly cost. 

10. Messaging and queueing
1) concepts
- message and queueing 
placing messages into a buffer is message and queueing. 

- payload
data contained within a message is called payload, which is protected until delivered. 

2) application architecture 
Applications are made of multiple components, which communicate w/ each other to transmit data, fulfil requests, and keep the application running. 
Example components: databases, servers, user interface, business logic, etc.

- tightly coupled architecture
If a single component fails, the other components and possibly the entire application fails. 
example: monolithic applications

- loosely coupled architecutre
Single failure won't cause cascading failures, which will help maintain application availability.
example: microservices approach with services and components to fulfill different functions. SNS and SQS are AWS's services to facilitate application integration. 
how: use buffers such as message queue between application A and B

3) Amazon Simple Queue Service (Amazon SQS)
- **SQS is a message queueing service**
For decoupled applications and microservices; you can send/store/receive messages btw software components at any volume, w/o losing messages or requiring other services to be available. 

- An application sends messages into a queue.

- A user/service retrieves a message from the queue, processes it, and then deletes it from the queue. 

4) Amazon Simple Notification Service (Amazon SNS)
- SNS topic
a channel for messages to be delivered. You can send one message to a topic, and it will fan out to all the subscribers in a single go. 

- publish/subscribe service model
**SNS is a pub/sub service. Using Amazon SNS topics, a publisher publishes messages to subscribers**.
Subscribers can choose to subscribe to a single topic or to multiple topics. 

- subscribers 
endpoints: AWS Lambda functions, SQS queue, web servers, HTTPS/HTTP web hooks, etc. 
fan out notifications to end users: mobile push, SMS, email. 

5) References

[Amazon SNS](https://aws.amazon.com/sns)

11. Additional compute services

1) Concepts
A. Serverless computing
- EC2 requires you set up and manage instance over time
patching instances when new software comes out, setting up the scaling of those instances, ensuring high availability of architected solutions.

- Serverless means you don't need to provision/manage these servers that your code runs on
you cannot actually see/access the underlying infrastructure or instances that are hosting your application. Instead, all the mgmt of the underlying environment from a provisioning, scaling, high availability, and maintenance perspective are taken care of. All you need to do is focus on the application. 

- serverless computing has the flexibility to scale serverless applications automatically
It can adjust the applications' capacity by modifying the units of consumption, such as throughput and memory. 

B. Containers
- allow you both the access to the underlying environment and efficiency and portability. 

- Docker container
Docker is a widely used platform which uses operating system level virtualization to deliver software in containers. It enables you to build/test/deploy apps quickly. 
Containers provide you with a standard way to package application's code, dependencies, and configurations into a single object. Containers can also be used for processes and workflows in which there are essential requirements for security, reliability, and scalability. 
Containers run on top of EC2 instances, and run in isolation from each other similar to virtual machines but with host being the EC2 instance.

- Container orchestration 
Container orchestration services help you deploy/manage/scale containerized applications. 
When using Docker containers on AWS, you need to processes to start/stop/restart/monitor containers running across a cluster (a number of EC2 instances together). 
Example container orchestration tools run on top of EC2: ECS, EKS. 

2) AWS Lambda
- serverless compute service for any application/backend service
AWS Lambda is a service that lets you run code w/o provisioning or managing servers. No containers/virtual machines, just code and configuration. 
It allows you to upload your code into a Lambda function, which configures a trigger that the service waits for. 

- trigger
When a trigger is detected, the code automatically run in a managed environment that is automatically scalable (whether it's 1 or 1000 incoming triggers), highly available, and all of the maintainance in the env itself is taken care of by AWS. 
Example: a simple Lambda function might involve automatically resizing uploaded images to the AWS Cloud. In this case, the function triggers when uploading a new image. 

- how AWS Lambda works
upload code to lambda, set code to trigger from an event source (AWS services, mobile applications, HTTP endpoints), Lambda code runs only when triggered, pay only for the compute time you use. 

- more suited for quick processing
Lambda is designed to run code under 15 mins, so it's not for deep learning, but more suited for quick processing like a web backend, handling requests, or a backend expense reporting processing service where each invocation takes less than 15 mins. 

3) Amazon Elastic Container Service (ECS)
ECS is a highly scalable, high-performance container mgmt system that enables you to run and scale containerized applications on AWS w/o managing your own container orchestration software. 
ECS supports Docker containers. AWS supports open-source Docker community Ed and subscription-based Docker Enterprise Ed. W/ ECS, you can use API calls to launch/stop Docker-enabled apps. 

4) Amazon Elastic Kubernetes Service (EKS)
EKS is a fully managed Kubernetes service on AWS.
Kubernetes is open-source software that enables you to deploy and manage containerized applications at scale. As new features and functionalities release for k8s apps, you can easily apply these updates to your applications managed by Amazon EKS. 

5) AWS Fargate
Fargate is a serverless compute engine for containers like ECS or EKS where you can run the code on, saving you the burden of provisioning/managing server infrastructure (underlying OS/EC2 instances management). 
You only pay for the resources that are required to run your containers. 

6) Summary of workflow
- use EC2
host traditional applications w/ full access to the underlying OS
- use AWS Lambda
host short running functions/service-oriented/event-driven applications, don't want to manage the underlying environment
- run Docker container-based workloads on AWS
first choose orchestration tool (ECS, or EKS),
then choose platform (EC2, or serverless env like AWS Fargate).

7) References

[AWS Lambda](https://aws.amazon.com/lambda)
[Amazon ECS](https://aws.amazon.com/ecs/)
[Docker](https://www.docker.com/)
[EKS](https://aws.amazon.com/eks/)
[Kubernetes](https://kubernetes.io/)
[AWS Fargate](https://aws.amazon.com/fargate/)
[Compute on AWS](https://aws.amazon.com/products/compute)

[AWS Compute Blog](https://aws.amazon.com/blogs/compute/)
[AWS Compute Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)
[Hands-On Tutorials: Compute](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute&awsf.getting-started-content-type=content-type%23hands-on)
[Category Deep Dive: Serverless](https://aws.amazon.com/getting-started/deep-dive-serverless/)
[AWS Customer Stories: Serverless](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23serverless)


### Module 3: Global Infrastructure and Reliability
#### Objectives
- Summarize the benefits of the AWS Global Infrastructure
- Describe the basic concept of Availability Zones
- Describe the benefits of Amazon CloudFront and Edge locations
- Compare different methods for provisioning AWS services


----------

### Module 4: Networking
#### Objectives
- Describe the basic concepts of networking
- Describe the difference between public and private networking resources
- Explain a virtual private gateway using a real life scenario
- Explain a virtual private network (VPN) using a real life scenario
- Describe the benefit of AWS Direct Connect
- Describe the benefit of hybrid deployments
- Describe the layers of security used in an IT strategy
- Describe which services are used to interact with the AWS global network


### Module 5: Storage and Databases
#### Objectives
- Summarize the basic concept of storage and databases
- Describe benefits of Amazon Elastic Block Store (Amazon EBS)
- Describe benefits of Amazon Simple Storage Service (Amazon S3)
- Describe the benefits of Amazon Elastic File System (Amazon EFS)
- Summarize various storage solutions
- Describe the benefits of Amazon Relational Database Service (Amazon RDS)
- Describe the benefits of Amazon DynamoDB
- Summarize various database services

### Module 6: Security
#### Objectives
- Explain the benefits of the shared responsibility model
- Describe multi-factor authentication (MFA)
- Differentiate between the AWS Identity and Access Management (IAM) security levels
- Describe security policies at a basic level
- Explain the benefits of AWS Organizations
- Summarize the benefits of compliance with AWS
- Explain primary AWS security services at a basic level

### Module 7: Monitoring and Analytics
#### Objectives
- Summarize approaches to monitoring your AWS environment
- Describe the benefits of Amazon CloudWatch
- Describe the benefits of AWS CloudTrail
- Describe the benefits of AWS Trusted Advisor

### Module 8: Pricing and Support
#### Objectives
- Understand AWS pricing and support models
- Describe the AWS Free Tier
- Describe key benefits of AWS Organizations and consolidated billing
- Explain the benefits of AWS Budgets
- Explain the benefits of AWS Cost Explorer
- Explain the primary benefits of the AWS Pricing Calculator
- Distinguish between the various AWS Support Plans
- Describe the benefits of AWS Marketplace

### Module 9: Migration and Innovation
#### Objectives
- Understand migration and innovation in the AWS Cloud
- Summarize the AWS Cloud Adoption Framework (AWS CAF)
- Summarize six key factors of a cloud migration strategy
- Describe the benefits of various AWS data migration solutions, such as AWS Snowcone, AWS Snowball, and AWS Snowmobile
- Summarize the broad scope of innovative solutions that AWS offers

### Module 10: The Cloud Journey
#### Objectives
- Summarize the five pillars of the AWS Well-Architected Framework
- Explain the six benefits of cloud computing

### Module 11: AWS Certified Cloud Practitioner Basics
#### Objectives
- Determine resources for preparing for the AWS Certified Cloud Practitioner examination
- Describe benefits of becoming AWS Certified