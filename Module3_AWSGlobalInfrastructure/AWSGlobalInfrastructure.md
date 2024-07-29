# AWS - Cloud Foundation

## Module 3 - AWS Global Infrastructure

### Section 1 - AWS Global Infrastructure

---

#### AWS Regions

AWS has the concept of `Region`, wich is a physical location around the world where  clusters data centers. Each group of logical data centers is an Availability Zone. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single data center, the multiple AZ design of every AWS region offers advantages for costumers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault-tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

AWS provides a more extensive global footprint than any other cloud provider, and to suport itsglobal footprint and ensure customers are served across the world, AWS opens new Regions rapidly. AWS maintains multiple geographic Regions, including Regions in Noth America, South America, Europe, China, Asia Pacific, Soth Africa, and the Middle East.

The resources of one region are isolated of another region. They are not automatically replicated between regions. If you need to replicate resources (data ou applications) between regions it's your responsability to do it.

You need to check the legal requirements of your business and country if exists any limitation about resources outside or inside of some region.

The global presence of AWS represnted by it's regions has a advantage to deliver low latence conenctions for yours customers.

Another point of atention is that some resources are available only at determinateds regions

South America (1)
---
* São Paulo

Asia Pacific and China (12)
---

* Beijing
* Honk Kong SAR
* Hyderabad
* Jakarta
* Melbourne
* Mumbai
* Ningxia
* Osaka
* Seoul
* Singapore
* Sydney
* Tokio

North America (8)
---

* AWS GovCloud (US-East)
* AWS GovCloud (US-West)
* CAnada Central
* Canada West
* Northern California
* Northern Virginia
* Ohio
* Oregon

Europe / Middle East / Africa (12)
---

* Bahrain
* Cape Town
* Europe (Stockholm)
* Frankfurt
* Ireland
* London
* Milan
* Paris
* Spain
* Tel Aviv
* UAE
* Zurich


#### Availability Zones
An Availability Zone Consists in one or more datacenters. You have to choice the selected AZ to store your application. The AZs are projected to isolate fails. AWS recomends data replication between AZs to resilience.

### Section 2 - AWS Services Categories and Services
---


AWS offers a broad set of a global cloud base products that can be used buinding blocks for common cloud architectures.

The AWS global infrastructure can be broken down in three elements: `Regions`, `Availability Zones` and `Point of Presence` wich include edge locations

The most used AWS Services:

1. `AWS Storage Services: ` 
   
   1. **S3 - AWS Simple Storage Service**: Object storage service that offers scalability data avalability, security and performance.
   2. **EBS - AWS Elastic Block Store**: High performance block storage designed for use with EC2 instances for workloads with high throughput 
   3. **AWS EFS - AWS Elastic File Server**: Scalable fully manager network file system, also knowed as NFS for use in AWS cloud services and local resources.
   4. **S3 Glacier**: Secure, durable and extremelly low cost S3 storage cloud service.
   

2. `AWS Compute Services: `
    
    1. **EC2 - Elastic Cloud Computing**: Provides resizeble compute capacity as virtual machines in the cloud.
    2. **EC2 Auto Scalling**: Enable to automatically add or remove EC2 instances acording conditions that you define.
    3. **ECS - Elastic Container Service**: High scalable and performance container orchestration service that suports docker containers.
    4. **ECR - Elastic Container Registry**: Fully docker manager container registry that makes it easy for developers to store, manager and deploy docker container images.
    5. **Beanstalk**: Service for deploying and scaling web applications in services and familiar servers such as Apache and Internet Information Services (IIS).
    6. **Lambda**: Enables to run code without provisioning or managing services. You pay only the compute time that you consume. There's no charge if your code are not running. 
    7. **EKS - Elastic Kubernetes Service**: Makes easy to deploy, manage and scale container applications that use kubernetes in AWS.
    8. **Fargate**: Compute engine for ECS that allows it to run container without having to manage servers or clusters. 
   
3. `AWS Database Services:`

    1. **RDS - Relational Databse Service**: Easy to setup, operate an scalable relational database in the cloud. It provides resizable capacity where automating time consume and administration tasks such as hardware provisioning, databese setup, pathing and backups.
    2. **Aurora**: MySql and PostgreSql comparable relational database. It's setup to be five times faster than standard MySql databases and three times faster than standard PostgreSql databases.
    3. **Redshift**: Enables do to run analytics queries against petabytes of data that store localy in the Amazon and deliver fast performance at any scale
    4. **DynamoDB**: Fully manage key value and document noSql database that deliver single digit milisecond performance at any scale with built in security, backup and restore and in memory cahing.

4. `Network and Content Delivery: ` 

    1. **VPC - Virtual Private Cloud**: Enables you to provisioning logicaly and isolated sections of AWS cloud to load AWS resources in a virtual network that you define.
    2. **Load Balancing**: Automatic distribuilting in comming application trafic accross multiple targets such as EC2 instances, containers, ip addresses and lambda functions.
    3. **CloudFront**: Fast content delivery network (CDN) that securely deliverys data, videos, applications and application programming interfaces to customers globally with latency and high transfers speeds.
    4. **Transit Gateway**: Enables customers to conect their VPC and their local networks to a single centrally managing gateway
    5. **Route 53**: Scalable cloud domain name system (DNS) web service designed to give you relyable way to route any users to the internet applications. 
    6. **Direct Connect**: Provides way to stablish dedicated private network connection from a datacenter or office to AWS wich can reduce significatly costs and increase bandwith throughput.
    7. **VPN - Virtual Private Network**: Provides a secure global network
 
 5. `Security, Identity and Compliance: ` 

    1. **IAM - Identity Access Management**: Enables you to manage access to aws services and resources securilly
    2. **Organizations**: Allows you to restrict wich services and actions are allowed in your accounts
    3. **Cognito**: Add user authentiication and access control to your web and mobile apps.
    4. **Artifact**: Provides on demand access to the aws security and compliance supports as well, the selected on line agreements.
    5. **KMS - Key Management Service**: Enables you to manage and create manage encrypting keys. You can use it to control the use of encription across the wide range of your AWS services in your applications
    6. **Shield**: Managed distribuided deny of service protection service that safe and guards applications running on AWS.
 
 6. `Costs and Management Services: `
   
    1. **Costs and Usage Report**: Wich contains the most comprehensive set of cost and usage of data available, includiting additional managed data about services, pricing and reservations.
    2. **Budgets**: Set custom budgets that alert you when your AWS cost or usage exceeds or the forecast exceed your budget amount.
    3. **Cost Explorer**: Enables you do visualize and understand and manage AWS cost usage over time.
 
 7. `Management and Governance Services: `

    1. **Management Console**: Service that is web's user interface for accessing your AWS account.
    2. **Config**: Service that helps you track resources inventory and changes. 
    3. **CloudWatch**: Allows you to monitor resources and applications.
    4. **Auto Scaling**: Provides features that allow you to scale multiple resources to meet demand.
    5. **CLI - Command Line Interface**: Provides a unified tool to manage AWS services.
    6. **Trusted Advisor**: On-line tool wich helps you optimize performance and security using AWS best practicies.
    7. **Well Architected Tool**: Wich provides help in reviwing and improving your workloads.
    8. **Cloud Trail**: Tracks user activity and API usage accross your AWS accounts.