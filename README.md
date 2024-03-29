# Cloud Computing 
Cloud computing is the on-demand availability of computing resources (such as storage and infrastructure), as services over the internet. Companies or individuals pay to access a virtual pool of shared resources, including compute, storage, and networking services, which are located on remote servers that are owned and managed by the service providers. This eliminates the need for individuals and businesses to self-manage physical resources, and only pay for what they use. 

When adopting cloud computing architecture, there is no one-size-fits-all. There are three different **cloud computing deployment models**: public cloud, private cloud, and hybrid cloud.
- Public Cloud are run by third-party cloud service providers in their location (edge). 
- Private Cloud are built, managed, and owned by a single organization and privately hosted in their own data centers (on-prem).
- Hybrid Cloud is a mixed computing environment where applications are run using a combination of computing, storage, and services deployed across public and private cloud.

There are three main types of **cloud computing service models** that you can select based on the level of control, flexibility, and management of business needs:
- Infrastructure as a service (IaaS) offers on-demand access to IT infrastructure services, including compute, storage, networking, and virtualization. It provides the highest level of control over IT resources and most closely resembles traditional on-premises IT resources.
- Platform as a service (PaaS) offers all the hardware and software resources needed for cloud application development. With PaaS, companies can focus fully on application development without the burden of managing and maintaining the underlying infrastructure.
- Software as a service (SaaS) delivers a full application stack as a service, from underlying infrastructure to maintenance and updates to the app software itself. A SaaS solution is often an end-user application, where both the service and the infrastructure is managed and maintained by the cloud service provider.

**Cloud-with-benefits**: 
- gives you ablity to scale elastically, both up or down as needed.
- hefty upfront costs of buying and maintaining on-prem hardware is eliminated (for public & hybrid  cloud ppl).
- Large distribution with high tech network facilities makes sure there exsists no down-time and slow responses (again for public & hybrid cloud ppl).  
- Cloud simplifies backup, disaster recovery, and business continuity as the data will be available in multiple locations.

**Amazon Web Services** provides a highly available technology infrastructure platform with multiple locations worldwide. 
- These locations are composed of regions (seperate geographical area) and Availability Zones (isolated locations in region).
- Availability Zones are physically separated within a typical metropolitan region and are located in lower-risk flood plains.
- They are provided with uninterruptable power supply and  redundantly connected to multiple tier-1 transit providers.
- This enables organizations to place resources and data in multiple locations around the globe. Helping to protect the confidentiality, integrity, and availability of systems and data is of utmost priority to AWS.

**AWS Cloud Computing Platform** provides more than 200 cloud computing services, The most commonly used are:
## Computational
#### Amazon EC2 (Elastic Compute Cloud):
- Purpose: Provides scalable compute capacity in the cloud.
- Used for: Hosting virtual servers to run applications, development, and testing.

#### AWS Lambda:
- Purpose: Serverless compute service that runs code in response to events.
- Used for: Building and running serverless applications, event-driven computing.

#### Amazon ECS (Elastic Container Service):
- Purpose: Highly scalable, high-performance container management service.
- Used for: Running, stopping, and managing Docker containers on a cluster.

#### Amazon Fargate:
- Purpose: Serverless compute engine for containers.
- Used for: Running containers without managing the underlying infrastructure. 

#### AWS Elastic Beanstack
- Purpose: Platform as a Service (PaaS) for deploying and managing applications.
- Used for: Simply deploy and scale your application without requiring any knowledge of underlying resource.

#### Amazon VPC (Virtual Private Cloud):
- Purpose: Provides a logically isolated section of the AWS Cloud where you can launch AWS resources.
- Used for: Building a secure and scalable network infrastructure within AWS.
  
## Storage
#### Amazon S3 (Simple Storage Service):
- Purpose: Object storage service for storing and retrieving any amount of data.
- Used for: Storing and retrieving data, backup and restore, static website hosting.

#### Amazon RDS (Relational Database Service):
- Purpose: Managed relational database service that simplifies database setup, operation, and scaling.
- Used for: Running and managing relational databases like MySQL, PostgreSQL, SQL Server, etc.

#### Amazon DynamoDB:
- Purpose: Fully managed NoSQL database service.
- Used for: Fast and flexible NoSQL database for applications with variable and high read/write workloads.


## EC-2
- Amazon EC2 is AWS primary web service that provides resizable compute capacity in the cloud. 
- Compute refers to the amount of computational power required to fulfill your workload.
- EC2 allows you to aquire compute through launching of virtual servers called instances.
- When instance is launched, you can compute according to your needs, as you would do with on-perm server. (will be charged based on hour the instance runs, not charged when stopped)
- The instance creation is initated by specifying the amount of virtual hardware dedicated to the instance and the software loaded on the instance.

virtual hardware:
There available instance types are based on the virtual CPU, memory, storage (size and type) and network performance.
family types like compute otimized, memory optimized, storage optimized, GPU-based instances. 

software:
Amazon Machine Image is a template that contains a software configuration (for example, an operating system, an application server, and applications). From an AMI, you launch an instance, which is a copy of the AMI running as a virtual server in the cloud. 
All are based on x86 OS, either Linux or Windows.




Elastic means flexibility not scalability.

Elastic load balancing distribute's and control the incoming traffic accross multiple EC2 instances in multiple AZ's to acheive greater level of fault tolerance.

Amazon CloudWatch is to monitor resources and applications running on AWS. collects metrics, log files and create alarm that send notifications.

Auto scaling gives you the advantage to resize the instance capacity up or down based on your variable workloads.


Health checks are done by elastic load balancing. Health check means to ensure traffic is not routed to unhealthy or failing instances. 

- for examples, you heavily rely on a EC2 instance or a S3 storage and it is experiencing issues. Health check will provide you rel time status about it.

Stick sesssion will enable load balancer to send all requests of the user's session to a specific instance.

You can auto-scale (done by  aws), maual scale (define max,min capacity), schedule scale (when there is predictable schedule), dynamic scale (define parameters that control auto-scale)

Authentication is verifying the identity of a user or system, while authorization is granting or denying access to specific resources based on the authenticated identity.

IAM allows you to control how people and programs are allowed to manipulate your AWS infrastructure.

MFA requires you to verify your identity with both something you know and something you have.

IAM Policy- effect, service, Amazon Resource Name
- Resource(IAM User) - arn:aws:iam:us-east-1:123456789012:user/David

Relational database, the data is stored in a predifined structed format like tables. The relationship between the tables are established using keys. verticle scaling. MySQL, Oracle
- Online Transaction Processing (OLTP) database system refers to transaction oriented applications that are frequently writing and changing data (e-commerce). Amazon RDS
- Online Analytical Processing (OLAP) database system is typically data warehouses and refers to reporting or analyzing large data sets. Amazon Redshift (data wharehouse)
  
Non-relational database, the data is stored in various structured formats like graph, file based. Horizantal scaling. MongoDB, Neo4j, Amazon Dynamo DB.

Recovery Point Objective (RPO) is defined as the maximum period of data loss that is acceptable in the event of a failure or incident. 

Recovery Time Objective (RTO) is defined as the maximum amount of downtime that is permitted to recover from backup and to resume processing.

