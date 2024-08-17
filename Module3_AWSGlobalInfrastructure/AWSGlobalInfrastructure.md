# AWS - Cloud Foundation

## Module 3 - AWS Global Infrastructure

### Section 1 - AWS Global Infrastructure

---

#### AWS Regions

AWS has the concept of a `Region`, wich is a physical location around the world where  clusters data centers. Each group of logical data centers is an Availability Zone. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single cata center, the multiple AZ design of every AWS region offers advantages for costumers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault-tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

AWS provides a more extensive global footprint than any other cloud provider, and to suport itsglobal footprint and ensure customers are served across the world, AWS opens new Regions rapidly. AWS maintains multiple geographic Regions, including Regions in Noth America, South America, Europe, China, Asia Pacific, Soth Africa, and the Middle East.

The resources of one region are isolated of another region. They are not automatically replicated between regions. If you need to replicate resources (data ou applications) between regions it's your responsability to do it.

You need to check the legal requirements and data governance of your business and country if exists any limitation about resources outside or inside of someone region.

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

Each AZ has any datacenters