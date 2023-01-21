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
Amazon Elastic File System
Serverless, fully elastic file storage   Amazon Elastic File System (EFS) automatically grows and shrinks as you add and remove files with no need for management or provisioning. autoscale/regional/direct connect /multiinstance r/w /linux file system 
RDBMS shift and lift 
![image](https://user-images.githubusercontent.com/33871532/213870242-5e17ee07-8072-4b58-896e-bb4aad23cec3.png)
Amazon Aurora
Each 10 GB chunk of your database volume is replicated six ways, across three Availability Zones. Amazon Aurora storage is fault-tolerant, transparently handling the loss of up to two copies of data without affecting database write availability and up to three copies without affecting read availability. Amazon Aurora storage is also self-healing; data blocks and disks are continuously scanned for errors and replaced automatically.

You can increase read throughput to support high-volume application requests by creating up to 15 database Amazon Aurora Replicas. Aurora Replicas share the same underlying storage as the source instance, lowering costs and avoiding the need to perform writes at the replica nodes. This frees up more processing power to serve read requests and reduces the replica lag time—often down to single-digit milliseconds. Aurora provides a reader endpoint so the application can connect without having to keep track of replicas as they are added and removed. It also supports auto-scaling, automatically adding and removing replicas in response to changes in performance metrics that you specify.

backup to s3 / point in time recovery 
https://aws.amazon.com/rds/aurora/features/

Amazon DynamoDB
Fast, flexible NoSQL database service for single-digit millisecond performance at any scale /serverless/non relational 
The primary key is the only required attribute for items in a table https://aws.amazon.com/dynamodb/faqs/

Amazon Redshift uses SQL to analyze structured and semi-structured data across data warehouses, operational databases, and data lakes, using AWS-designed hardware and machine learning to deliver the best price performance at any scale.(for old data , ended in the past)
AWS Database Migration Service (AWS DMS) is a managed migration and replication service that helps move your database and analytics workloads to AWS quickly, securely, and with minimal downtime and zero data loss.

AWS Schema Conversion Tool
AWS offers two schema conversion solutions to make heterogeneous database migrations predictable, fast, secure, and simple. Customers have the choice to: 1) log in to the AWS Database Migration Service (AWS DMS) console to initiate the AWS DMS Schema Conversion (DMS SC) workflow for a fully managed experience or 2) download the AWS Schema Conversion Tool (AWS SCT) software to their local drive.

Amazon DocumentDB (with MongoDB compatibility)
Scale enterprise workloads with ease using a fully managed native JSON document database

Amazon Neptune is a fully managed database service built for the cloud that makes it easier to build and run graph applications. Neptune provides built-in security, continuous backups, serverless compute, and integrations with other AWS services. social media 

Amazon Managed Blockchain is a fully managed service that makes it easy to join public networks or create and manage scalable private networks using the popular open-source frameworks Hyperledger Fabric and Ethereum.

Amazon Quantum Ledger Database (QLDB) is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log.

Amazon ElastiCache is a fully managed, in-memory caching service supporting flexible, real-time use cases. You can use ElastiCache for caching, which accelerates application and database performance, or as a primary data store for use cases that don't require durability like session stores, gaming leaderboards, streaming, and analytics. ElastiCache is compatible with Redis and Memcached. 

Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB that delivers up to a 10 times performance improvement—from milliseconds to microseconds—even at millions of requests per second.

AWS responsibility “Security of the Cloud”  + Customer responsibility “Security in the Cloud”

root user =owner = do anything 
AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can centrally manage permissions that control which AWS resources users can access. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

Apply least-privilege permissions

iam policy -> iam user 
groups-roles-policies-users 
roles -> temporary 

![image](https://user-images.githubusercontent.com/33871532/213871026-972d2fb5-7bad-493b-ae5d-687ce7ce9239.png) 
organizational units-service contol policies 
![image](https://user-images.githubusercontent.com/33871532/213871082-b24aaa9a-7dad-494f-950b-0262f0ba33c3.png)
![20230121_172239](https://user-images.githubusercontent.com/33871532/213871186-69733fcc-967e-4b83-aad6-b6ae0e544d94.jpg)
Amazon Inspector is an automated vulnerability management service that continually scans AWS workloads for software vulnerabilities and unintended network exposure.
Amazon GuardDuty is a threat detection service that continuously monitors your AWS accounts and workloads for malicious activity and delivers detailed security findings for visibility and remediation.(analize metadeta)
AWS Key Management Service (AWS KMS) lets you create, manage, and control cryptographic keys across your applications and more than 100 AWS services.
![image](https://user-images.githubusercontent.com/33871532/213871265-04cf832f-09cb-4ace-9800-ba5caf19d79b.png)
AWS CloudTrail
Capture and consolidate user activity and API usage across AWS Regions and accounts on a single, centrally controlled platform.
![image](https://user-images.githubusercontent.com/33871532/213871354-82759b9d-14c7-48ad-bfed-c83da7eb1383.png)
AWS Trusted Advisor provides recommendations that help you follow AWS best practices. Trusted Advisor evaluates your account by using checks. These checks identify ways to optimize your AWS infrastructure, improve security and performance, reduce costs, and monitor service quotas. You can then follow the recommendations to optimize your services and resources.
aws free
Types Of Offers
Explore more than 100 products and start building on AWS using the Free Tier. Three different types of free offers are available
depending on the product used. Click icon below to explore our offers.

Free trials
Free trials
Short-term free trial offers start from the date you activate a particular service
12 months free
12 months free
Enjoy these offers for 12-months following your initial sign-up date to AWS
Always free
Always free
These free tier offers do not expire and are available to all AWS customers

https://aws.amazon.com/free/


Pay-as-you-go
Pay-as-you-go allows you to easily adapt to changing business needs without overcommitting budgets and improving your responsiveness to changes. With a pay-as-you-go model, you can adapt your business depending on need and not on forecasts, reducing the risk of overprovisioning or missing capacity.

Read more »

Save when you commit
For AWS Compute and AWS Machine Learning, Savings Plans offer savings over On-Demand in exchange for a commitment to use a specific amount (measured in $/hour) of an AWS service or a category of services, for a one- or three-year period.
Read more »

Pay less by using more
With AWS, you can get volume based discounts and realize important savings as your usage increases. For services such as S3, pricing is tiered, meaning the more you use, the less you pay per GB. AWS also gives you options to acquire services that help you address your business needs.

Read more »

organizations offer consilidated buying for org owners 
You can use AWS Budgets to track and take action on your AWS costs and usage.
A Technical Account Manager (TAM) is your designated technical point of contact who helps you onboard, provides advocacy and guidance to help plan and build solutions using best practices, coordinates access to subject matter experts, assists with case management, presents insights and recommendations on your AWS spend, workload optimization, and event management, and proactively keeps your AWS environment healthy.

https://aws.amazon.com/premiumsupport/plans/ (see table here )
AWS Marketplace
Simplify procurement, provisioning, and governance of third-party software, services, and data

AWS Cloud Adoption Framework (AWS CAF)
Business
The Business perspective helps ensure that your cloud investments accelerate your digital transformation ambitions and business outcomes. Common stakeholders include chief executive officer (CEO), chief financial officer (CFO), chief operations officer (COO), chief information officer (CIO), and chief technology officer (CTO).
Read Whitepaper »

People
The People perspective serves as a bridge between technology and business, accelerating the cloud journey to help organizations more rapidly evolve to a culture of continuous growth, learning, and where change becomes business-as-normal, with focus on culture, organizational structure, leadership, and workforce. Common stakeholders include CIO, COO, CTO, cloud director, and cross-functional and enterprise-wide leaders.
Governance
The Governance perspective helps you orchestrate your cloud initiatives while maximizing organizational benefits and minimizing transformation-related risks. Common stakeholders include chief transformation officer, CIO, CTO, CFO, chief data officer (CDO), and chief risk officer (CRO).
Read Whitepaper »

Platform
The Platform perspective helps you build an enterprise-grade, scalable, hybrid cloud platform, modernize existing workloads, and implement new cloud-native solutions. Common stakeholders include CTO, technology leaders, architects, and engineers.
Security
The Security perspective helps you achieve the confidentiality, integrity, and availability of your data and cloud workloads. Common stakeholders include chief information security officer (CISO), chief compliance officer (CCO), internal audit leaders, and security architects and engineers.
Operations
The Operations perspective helps ensure that your cloud services are delivered at a level that meets the needs of your business. Common stakeholders include infrastructure and operations leaders, site reliability engineers, and information technology service managers.
https://aws.amazon.com/professional-services/CAF/
![image](https://user-images.githubusercontent.com/33871532/213871705-fcf2318f-40fb-48be-ae40-febe442b86ee.png)
AWS Snowcone
AWS Snowcone is the most compact and portable device. Weighing in at 4.5 pounds (2.1 kg) and available with SSD or HDD options, Snowcone is ruggedized, secure, and purpose-built for use outside of a traditional data center.

Learn more »
AWS Snowball
AWS Snowball is available as a Compute Optimized device or a Storage Optimized device. Explore the options best suited for your needs. All devices are suited for extreme conditions, tamper proof, and highly secure.
Learn more »
AWS Snowmobile
AWS Snowmobile is an Exabyte-scale data migration device used to move extremely large amounts of data to AWS. Migrate up to 100PB in a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck.
https://aws.amazon.com/snow/
Amazon SageMaker
Build, train, and deploy machine learning (ML) models for any use case with fully managed infrastructure, tools, and workflows
Amazon Augmented AI (A2I) allows you to conduct a human review of machine learning (ML) systems to guarantee precision.

Amazon Lex is a fully managed artificial intelligence (AI) service with advanced natural language models to design, build, test, and deploy conversational interfaces in applications.(Alexa)
Amazon Textract is a machine learning (ML) service that automatically extracts text, handwriting, and data from scanned documents.
AWS DeepRacer gives you an interesting and fun way to get started with reinforcement learning (RL). RL is an advanced machine learning (ML) technique that takes a very different approach to training models than other machine learning methods. Its super power is that it learns very complex behaviors without requiring any labeled training data, and can make short term decisions while optimizing for a longer term goal.

AWS Ground Station is a fully managed service that lets you control satellite communications, process data, and scale your operations without having to worry about building or managing your own ground station infrastructure

Amazon Comprehend is a natural-language processing (NLP) service that uses machine learning to uncover valuable insights and connections in text.
Amazon Transcribe Automatically convert speech to text
Amazon Fraud Detector Detect online fraud faster with machine learning
The AWS Well-Architected Framework documents a set of foundational questions that allow you to understand if a specific architecture aligns well with cloud best practices. 
Name	Description
Operational excellence	The ability to support development and run workloads effectively, gain insight into their operations, and to continuously improve supporting processes and procedures to deliver business value.
Security	The security pillar describes how to take advantage of cloud technologies to protect data, systems, and assets in a way that can improve your security posture.
Reliability	The reliability pillar encompasses the ability of a workload to perform its intended function correctly and consistently when it’s expected to. This includes the ability to operate and test the workload through its total lifecycle. This paper provides in-depth, best practice guidance for implementing reliable workloads on AWS.
Performance efficiency	The ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.
Cost optimization	The ability to run systems to deliver business value at the lowest price point.
Sustainability	The ability to continually improve sustainability impacts by reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benefits from the provisioned resources and minimizing the total resources required.
https://docs.aws.amazon.com/wellarchitected/latest/framework/definitions.html
The AWS Well-Architected Tool is designed to help you review the state of your applications and workloads against architectural best practices, identify opportunities for improvement, and track progress over time.

https://aws.amazon.com/well-architected-tool/

donate to 1000plus https://www.1000plus.am/en/donation-types/

send dogecoin : DSVzLygz33XaFXPtkJUxpASAf9Khgtfoo9 




















