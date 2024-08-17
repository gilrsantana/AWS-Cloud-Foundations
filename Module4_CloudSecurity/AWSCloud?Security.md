# AWS - Cloud Foundation

## Module 4 - AWS Cloud Security

### Section 1 - AWS Shared Responsability

---
AWS Shared Responsability basicaly indicates wich parts of security will be handle by AWS or wich parts customers are responsable for. We can say that AWS is responsable for the security of the cloud, that means AWS is responsable for everything related to the phisical implementation, this includes phisical facilities and systems. According to the model, customers are responsable for security in the cloud, that means customers are responsable for secure every application and dataset that it implement in the cloud. AWS provides the tools to protect your applications and data, however it is your responsability to use this tools to secure your data and applications. 

AWS operates, manage and controls the software virtualization layer and hardware in global infrasestructure components wich the phisical security of the facilities where the AWS services operates. AWS is responsable for protecting the infrastructure including the hardware, software, networking and facilities that run the AWS cloud services. Meanwhile, the customer reponsable for the encryption of data and rest and the encryption of data in transit from one system to another. The customer should also ensure that the network is confugured for security. The customer should ensure that security credentials and loggins are managed safely. The customer should also manage the firewall configurations and the security of the operating system in applications that run on any compute instances they lauch, for example using the Amazon EC2 Services.

AWS ensures that the virtualization infraestructure provides isolation between customer's workloads for example, the EC2 instances of one customer are isolated from compute environment from another customer.

### Section 2 - AWS Identity and Access Management (IAM)

---

Identity and Access Management is one of the first services you would use in AWS. This is the service wich allows you to define users and the types of access that would will be allow to have. It's a free service. There is no charge for you in order to define users, groups, rolls and access controls. It's a global service, that means that IAM resources are available to all regions of the AWS cloud, allowing you to control access to all your AWS services using policies and assign them to the specific users in order to define operational groups like systems administrators, database administrators, storage administrators and security administratos. 

It can handle authentication and verification of access for user, roll or to specific resource. In a nutshell IAM is a tool that centrally manages access to launching, configuring, managing and terminating resources in your AWS account. It provides a fine grain control over access to resouces including the management of who can access the resources and how they can be accessed. You can grant diferent permissions to diferent people or even applications.

IAM allows you to define some items that require definition. 

1. **User:** is usually a person that has been allowed to access your AWS account. Each user must have a unique name with no spaces in the name and should be assigned way to identify it self something as simple as a password will work. 

2. **Group:** is an eficient mecanism to apply permissions. Basically, you define a group and apply access policies to it. You them can add and remove users to the group without needing to atach policies directly to each user. Groups are usefull to carefully define access to diferent responsability teams like DBAs, developers and auditors.

3. **Policies:** is document wich define access to one or more services. They are created independently of users and groups. They can them be atache in order to enable the access controls that they define.

4. **Roll:** is mechanism of granting temporally access to AWS services, for example, an user can assume a roll to access a service that is not normally available. 