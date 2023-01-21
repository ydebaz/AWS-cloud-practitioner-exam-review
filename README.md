# AWS-cloud-practitioner-exam-review
this is a review paper for aws cloud practitioner exam , you will need this paper 3 times :
1. print it before you start studying for the exam and write your extra notes on it while studying 
2. open this repo 2 hours before the exam and open all the links one by one , spend around 30 seconds on each topic 
3. take your printed papers with you to the exam center and read it once more 30 minutes before the exam 

remember to take 2 forms of id with you 

1. EC2 https://aws.amazon.com/ec2/
2. pay for running /not stopped /not terminated /share host with other instances / virtualization tech 
3. sharing physical resources /hypervisor https://www.quora.com/What-is-the-hypervisor-in-AWS
4. multitenancy / vertical scaling 
5. ![image](https://user-images.githubusercontent.com/33871532/213867455-1472b52c-5717-4349-aabf-30cbe7c10b89.png)
AWS responsibility “Security of the Cloud” - AWS is responsible for protecting the infrastructure that runs all of the services offered in the AWS Cloud. This infrastructure is composed of the hardware, software, networking, and facilities that run AWS Cloud services.

Customer responsibility “Security in the Cloud” – Customer responsibility will be determined by the AWS Cloud services that a customer selects. This determines the amount of configuration work the customer must perform as part of their security responsibilities. For example, a service such as Amazon Elastic Compute Cloud (Amazon EC2) is categorized as Infrastructure as a Service (IaaS) and, as such, requires the customer to perform all of the necessary security configuration and management tasks. Customers that deploy an Amazon EC2 instance are responsible for management of the guest operating system (including updates and security patches), any application software or utilities installed by the customer on the instances, and the configuration of the AWS-provided firewall (called a security group) on each instance. For abstracted services, such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data. Customers are responsible for managing their data (including encryption options), classifying their assets, and using IAM tools to apply the appropriate permissions.

https://aws.amazon.com/compliance/shared-responsibility-model/

launch connect use
![image](https://user-images.githubusercontent.com/33871532/213867543-22384074-c8ef-41cd-9988-c3f4646869a4.png)
General purpose instances provide a balance of compute, memory, and networking resources, and can be used for a wide range of workloads.
Compute optimized instances are ideal for compute-bound applications that benefit from high-performance processors.
Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.

Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver tens of thousands of low-latency, random I/O operations per second (IOPS) to applications.
Accelerated computing instances use hardware accelerators, or co-processors, to perform some functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs. These instances enable more parallelism for higher throughput on compute-intensive workloads.

On-Demand Instances
Pay for the instances that you use by the second, with a minimum of 60 seconds, with no long-term commitments or upfront payments.

Savings Plans
You can reduce your Amazon EC2 costs by making a commitment to a consistent amount of usage, in USD per hour, for a term of 1 or 3 years.

Reserved Instances
You can reduce your Amazon EC2 costs by making a commitment to a specific instance configuration, including instance type and Region, for a term of 1 or 3 years.

Spot Instances
Request unused EC2 instances, which can reduce your Amazon EC2 costs significantly.

Dedicated Instances are Amazon EC2 instances that run in a VPC on hardware that's dedicated to a single customer. Your Dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts. Dedicated instances may share hardware with other instances from the same AWS account that are not Dedicated instances. Pay for Dedicated Instances On-Demand, save up to 70% by purchasing Reserved Instances, or save up to 90% by purchasing Spot Instances.

You can also use Dedicated Hosts to launch Amazon EC2 instances on physical servers that are dedicated for your use. Dedicated Hosts give you additional visibility and control over how instances are placed on a physical server, and you can reliably use the same physical server over time. As a result, Dedicated Hosts enable you to use your existing server-bound software licenses like Windows Server and address corporate compliance and regulatory requirements. 

Characteristic

Standard

Convertible

Terms (avg. discount off On-Demand)

1yr (40%), 3yr (60%)

1yr (31%), 3yr (54%)

Change Availability Zone, instance size (for Linux OS), networking type

Yes (Using ModifyReservedInstances API and console)

Yes (Using ExchangeReservedInstances API and console)

Change instance families, operating system, tenancy, and payment option

 

Yes

Benefit from Price Reductions
 	Yes
  
  https://aws.amazon.com/ec2/pricing/reserved-instances/
  
  ![image](https://user-images.githubusercontent.com/33871532/213867779-12f2d961-c063-4e0b-a2a1-50c555e9c3a6.png)
  Increase availability with predictive or dynamic scaling policies with the right amount of compute capacity.
  scalability 
  
  Elastic Load Balancing
Distribute network traffic to improve application scalability
https://aws.amazon.com/elasticloadbalancing/

![image](https://user-images.githubusercontent.com/33871532/213867963-27c8934c-f666-4c92-9ac9-6fe085953498.png)

tight ->monolithic -> one fail / all fail 
loose -> micro services -> no fail 
Amazon SQS
Fully managed message queuing for microservices, distributed systems, and serverless applications
https://aws.amazon.com/sqs/
Amazon Simple Queue Service (SQS) lets you send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available.
Amazon Simple Notification Service (SNS) sends notifications two ways, A2A and A2P. A2A provides high-throughput, push-based, many-to-many messaging between distributed systems, microservices, and event-driven serverless applications. These applications include Amazon Simple Queue Service (SQS), Amazon Kinesis Data Firehose, AWS Lambda, and other HTTPS endpoints. A2P functionality lets you send messages to your customers with SMS texts, push notifications, and email. 

https://aws.amazon.com/sns/
sns create topic , send to endpoints , to end users using , push sms email 
serverless cant see or access underlying arch 
aws lambda (under 15 minutes ) https://aws.amazon.com/lambda/
Amazon ECS is a fully managed container orchestration service that helps you easily deploy, manage, and scale containerized applications. It deeply integrates with the rest of the AWS platform to provide a secure and easy-to-use solution for running container workloads in the cloud and now on your infrastructure with Amazon ECS Anywhere.
https://aws.amazon.com/ecs/
Amazon EKS is a managed Kubernetes service to run Kubernetes in the AWS cloud and on-premises data centers. In the cloud, Amazon EKS automatically manages the availability and scalability of the Kubernetes control plane nodes responsible for scheduling containers, managing application availability, storing cluster data, and other key tasks. With Amazon EKS, you can take advantage of all the performance, scale, reliability, and availability of AWS infrastructure, as well as integrations with AWS networking and security services. On-premises, EKS provides a consistent, fully-supported Kubernetes solution with integrated tooling and simple deployment to AWS Outposts, virtual machines, or bare metal servers. https://aws.amazon.com/eks/

docker orchestration tools

AWS Fargate is a serverless, pay-as-you-go compute engine that lets you focus on building applications without managing servers. AWS Fargate is compatible with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS)

container package code + dependencies into single object 

Evaluating Regions for deployment
There are four main factors that play into evaluating each AWS Region for a workload deployment:

Compliance. If your workload contains data that is bound by local regulations, then selecting the Region that complies with the regulation overrides other evaluation factors. This applies to workloads that are bound by data residency laws where choosing an AWS Region located in that country is mandatory.
Latency. A major factor to consider for user experience is latency. Reduced network latency can make substantial impact on enhancing the user experience. Choosing an AWS Region with close proximity to your user base location can achieve lower network latency. It can also increase communication quality, given that network packets have fewer exchange points to travel through.
Cost. AWS services are priced differently from one Region to another. Some Regions have lower cost than others, which can result in a cost reduction for the same deployment.
Services and features. Newer services and features are deployed to Regions gradually. Although all AWS Regions have the same service level agreement (SLA), some larger Regions are usually first to offer newer services, features, and software releases. Smaller Regions may not get these services or features in time for you to use them to support your workload.

Amazon Braket
Accelerate quantum computing research
https://aws.amazon.com/braket/

ELB runs across avalaiblity zones 

![image](https://user-images.githubusercontent.com/33871532/213868462-6e012703-31f2-43ef-b84b-38d56b9974e5.png)
![image](https://user-images.githubusercontent.com/33871532/213868512-67610c2e-a909-4a73-bc30-70db833b5ed1.png)

Amazon CloudFront is a content delivery network (CDN) service built for high performance, security, and developer convenience.
https://aws.amazon.com/cloudfront/
uses cache 

Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. Route 53 connects user requests to internet applications running on AWS or on-premises.

https://aws.amazon.com/route53/

AWS Outposts Family
Run AWS infrastructure and services on premises 
https://docs.aws.amazon.com/outposts/latest/userguide/what-is-outposts.html 

in aws everything is an api call

![image](https://user-images.githubusercontent.com/33871532/213868723-60592825-07c0-4fe0-9816-8abc5dc80d4e.png)
The AWS Command Line Interface (AWS CLI) is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.
AWS sdk for code 

AWS Elastic Beanstalk

Elastic Beanstalk is a service for deploying and scaling web applications and services. Upload your code and Elastic Beanstalk automatically handles the deployment—from capacity provisioning, load balancing, and auto scaling to application health monitoring.
![image](https://user-images.githubusercontent.com/33871532/213868831-844114be-026f-41f4-98ce-3c0a101c08e4.png)

Amazon Virtual Private Cloud (Amazon VPC)
Customize your virtual network by choosing your own IP address range, creating subnets, and configuring route tables.
Amazon Virtual Private Cloud (Amazon VPC) gives you full control over your virtual networking environment, including resource placement, connectivity, and security. Get started by setting up your VPC in the AWS service console. Next, add resources to it such as Amazon Elastic Compute Cloud (EC2) and Amazon Relational Database Service (RDS) instances. Finally, define how your VPCs communicate with each other across accounts, Availability Zones, or AWS Regions. In the example below, network traffic is being shared between two VPCs within each Region.

![image](https://user-images.githubusercontent.com/33871532/213868986-ccce0ce8-571d-4412-a5f3-5be9bd2a871c.png)
public -> internet gateway 
private -> vp gateway ->AWS direct connect 
![image](https://user-images.githubusercontent.com/33871532/213869035-c70a2b50-0cd3-4040-9057-4f87c88ccc8b.png) 
https://aws.amazon.com/directconnect/
![image](https://user-images.githubusercontent.com/33871532/213869081-cb8b846f-fcde-4673-b398-2b83308a13c6.png)
![image](https://user-images.githubusercontent.com/33871532/213869089-5f0c0c34-5761-4fc9-9012-4407e206cbac.png)

Amazon Elastic Block Store (EBS)
snapshots/incremental backup https://aws.amazon.com/ebs/

Amazon Simple Storage Service (Amazon S3) data stored in buckets as objects up to 5tb /version objects 
Amazon S3 Standard (S3 Standard) stored in 3 facilities (az)
You can use Amazon S3 to host a static website. On a static website, individual webpages include static content. They might also contain client-side scripts.

S3 Standard-Infrequent Access (S3 Standard-IA) and S3 One Zone-Infrequent Access (S3 One Zone-IA) for less frequently accessed data (backups)
S3 Glacier Instant Retrieval for archive data that needs immediate access, S3 Glacier Flexible Retrieval (formerly S3 Glacier) for rarely accessed long-term data that does not require immediate access, and Amazon S3 Glacier Deep Archive (S3 Glacier Deep Archive) for long-term archive and digital preservation with retrieval in hours at the lowest cost storage in the cloud. If you have data residency requirements that can’t be met by an existing AWS Region, you can use the S3 Outposts storage class to store your S3 data on premises.
Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering) is the first cloud storage that automatically reduces your storage costs on a granular object level by automatically moving data to the most cost-effective access tier based on access frequency, without performance impact, retrieval fees, or operational overhead. S3 Intelligent-Tiering delivers milliseconds latency and high throughput performance for frequently, infrequently, and rarely accessed data in the Frequent, Infrequent, and Archive Instant Access tiers. You can use S3 Intelligent-Tiering as the default storage class for virtually any workload, especially data lakes, data analytics, new applications, and user-generated content.
https://aws.amazon.com/s3/storage-classes/?nc=sn&loc=3











