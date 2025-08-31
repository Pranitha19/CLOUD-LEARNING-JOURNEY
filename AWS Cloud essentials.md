# CLOUD-LEARNING-JOURNEY

# Week 1: Introduction to Cloud
Learned about different cloud deployment types

Learned what is cloud computing and its benefits
Cloud-based deployment : Applications and services are hosted on cloud infrastructure (e.g., AWS, Azure, GCP) and accessed over the internet.

On-premises deployment : Applications are installed and run on servers physically located within the organization's facilities.

Hybrid deployment : A mix of cloud and on-premises infrastructure working together.


| Feature     | Cloud-Based                  | On-Premises          | Hybrid                         |
| ----------- | ---------------------------- | -------------------- | ------------------------------ |
| Ownership   | Cloud Provider               | Organization         | Shared                         |
| Location    | Remote                       | On-site              | Both                           |
| Control     | Low                          | Full                 | Partial                        |
| Scalability | High                         | Limited              | High (via cloud)               |
| Maintenance | Provider-managed             | Organization-managed | Shared                         |
| Best For    | Fast, cost-effective scaling | High-security needs  | Balanced flexibility & control |

# Benefits:

    Stop guessing capacity: we can dynamically increase the storage or any other services by capacity anytime. 
    With the AWS Cloud, the company can conveniently scale resources up or down based on actual demand, eliminating the need to guess future capacity requirements. 
    Stop spending money to run and maintain data centers Go global in minutes: we can use it from anyuwhere in the world just by changing aws region. 
    Trade fixed expense for variable expense: By using the AWS Cloud, businesses can transition from fixed investments to variable costs. 
    With variable costs, customer expenses are better aligned with actual usage, thus creating more financial flexibility.

# Week 2: Launching an EC2 Instance (Lab 1):

I have Launched an amazon EC2 Instance for first time in AWS Console.
To launch an EC2 instance for a web server, configure the AMI to define the operating system and software; 
select the instance type to allocate CPU, memory, and storage; and set up storage options, including the type and size of the volume.

Load balancing, permissions, and instance termination behavior are not required when launching a basic Amazon EC2 web server.

All interactions with services are powered by APIs. You can access these APIs through three primary methods: the AWS Management Console, the AWS CLI, or the AWS SDK. Let's review these methods.

<img width="1680" height="439" alt="image" src="https://github.com/user-attachments/assets/35f64074-c98c-4565-8456-66c20fb5c4f4" />


The AWS Management Console is a web interface for managing AWS services, offering quick access to services, search functionality, and simplified workflows. With the mobile app, you monitor resources, view alarms, and check billing, supporting multiple logged-in identities at once. Good for: Users who prefer a visual, easy-to-use interface for managing and configuring AWS services

With the AWS CLI, you manage multiple AWS services directly from the command line across Windows, macOS, and Linux. You can automate tasks through scripts, such as launching EC2 instances. Good for: Advanced users and developers who need to automate tasks, script actions, and manage AWS resources efficiently from the command line

The AWS SDK simplifies integrating AWS services into your applications by providing APIs for various programming languages. AWS offers documentation and sample code for languages like C++, Java, and .NET to help you get started. Good for: Developers looking to integrate AWS services into their applications using language-specific APIs

The AWS CLI enables automation through scripting, which is more efficient and reduces manual errors compared to the console.

The customer handles the operating system, networking, and applications on the EC2 instances. AWS manages the hardware.

 # Compute and shared responsibility model

The AWS Shared Responsibility Model outlines the division of duties between the customer and AWS. 

AWS handles the security of the cloud (hardware and infrastructure), whereas the customer is responsible for security in the cloud (applications, data, and access control).

service characteristics and security

# IaaS:
    Customers has more flexibility over configuring networking and storage. 
    customer is responsible for more aspects of security. customer configures the access control. 
    Example services managed by customer are Amazon EC2, Amazon VPC, Amazon EBS.
# PaaS:
    Customer does not need to manage the underlying indrastructure. 
    AWS manage the operating System, Database patching, firewall configuration and disaster recovery. Customers can focus more on managing code or data. 
    Example services provided by AWS are amazon Lambda, Amazon RDS and AWS Elastic Beanstalk.
# Saas:
    Software is centrally hosted. Liscensed on a subscription model or pay-as-you-go basis. 
    Services are typically accesed by a web browser or mobile app or API. customers do  not need to manage the infrastucture that supports the service.
    Examples of Saas are AWS trusted advisor, AWS shield, Amazon Chime.
  
---> Amazon Machine Images:

 
 An AMI includes the operating system, storage setup, architecture type, permissions for launching, and any extra software that is already installed. You can use one AMI to launch several EC2 instances that all have the same setup.

 An AMI is a pre-configured virtual machine image that contains the operating system, application server, and applications. This helps to launch EC2 instances quickly with the desired software and settings.


<img width="1680" height="844" alt="image" src="https://github.com/user-attachments/assets/b760f01b-c935-4097-895e-c8f9c22575b7" />

---> Three ways to use AMIs 
                           
 First, you can create your own by building a custom AMI with specific configurations and software tailored to your needs. 
    Second, you can use pre-configured AWS AMIs, which are set up for common operating systems and software. 
    Lastly, you can purchase AMIs from the AWS Marketplace, where third-party vendors offer specialized software designed for specific use cases.


<img width="1680" height="641" alt="image" src="https://github.com/user-attachments/assets/287f6b87-439e-460c-87fe-25fb36e1d8eb" />

# AWS pricing options

On-Demand Instances: Pay only for the compute capacity you consume with no upfront payments or long-term commitments required.

 Reserved Instances: Get a savings of up to 75 percent by committing to a 1-year or 3-year term for predictable workloads using specific instance families and AWS Regions.

 Spot Instances: Bid on spare compute capacity at up to 90 percent off the On-Demand price, with the flexibility to be interrupted when AWS reclaims the instance.

 Savings Plans: Save up to 72 percent across a variety of instance types and services by committing to a consistent usage level for 1 or 3 years.

 Dedicated Hosts: Reserve an entire physical server for your exclusive use. This option offers full control and is ideal for workloads with strict security or licensing needs.

Dedicated Instances: Pay for instances running on hardware dedicated solely to your account. This option provides isolation from other AWS customers.

# Week 4: AWS Identity and Access Management

AWS Identity and Access Management (IAM) is a web service that enables Amazon Web Services (AWS) customers to manage users and user permissions in AWS. With IAM, you can centrally manage users, security credentials such as access keys, and permissions that control which AWS resources users can access.


AWS Identity and Access Management (IAM) can be used to:

Manage IAM Users and their access: You can create Users and assign them individual security credentials (access keys, passwords, and multi-factor authentication devices). You can manage permissions to control which operations a User can perform.

Manage IAM Roles and their permissions: An IAM Role is similar to a User, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a Role is intended to be assumable by anyone who needs it.

Manage federated users and their permissions: You can enable identity federation to allow existing users in your enterprise to access the AWS Management Console, to call AWS APIs and to access resources, without the need to create an IAM User for each identity.


# Lab 2: Introduction to AWS IAM

Worked on lab2 with precreated users and groups(with policies) and all users username and passwords.


 <img width="2200" height="1100" alt="image" src="https://github.com/user-attachments/assets/007f1f73-d5c6-41b4-9706-131753371918" />
 

TASK 1 - Added user-1 to S3-Support group	
TASK 2 - Added user-2 to EC2-Support group	
TASK 3 - Added user-3 to EC2-Admin group	
TASK 4 - user-1 logged in	
TASK 5 - user-2 logged in	
TASK 6 - user-2 ec2 stop instance attempt
TASK 7 - user-3 logged in	
TASK 8 - user-3 EC2 stop instance attempt	

# Resources:
AWS documentation
AWS Skill builder (course enrolled)


