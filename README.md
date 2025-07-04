# CLOUD-LEARNING-JOURNEY
Welcome to my personal learning journal! This repository tracks my progress as I learn and grow in the field of Cloud!
Why I Started
I created this repo to:
- Document everything I learn
- Track my weekly/monthly goals
- Build a habit of consistent progress
- Share my learning path with others

  
# Week 1: Introduction to Cloud
- Learned about different cloud deployment types
- - Learned what is cloud computing and its benefits
  
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



  On-Demand delivery of it resources over the internet with pay-as-you-go pricing.
  
Benefits:

Stop guessing capacity: we can dynamically increase the storage or any other services by capacity anytime. With the AWS Cloud, the company can conveniently scale resources up or down based on actual demand, eliminating the need to guess future capacity requirements.
Stop spending money to run and maintain data centers
Go global in minutes: we can use it from anyuwhere in the world just by changing aws region.
Trade fixed expense for variable expense: By using the AWS Cloud, businesses can transition from fixed investments to variable costs. With variable costs, customer expenses are better aligned with actual usage, thus creating more financial flexibility.

# Week 2: Interacting with AWS services
--> Launched an amazon EC2 Instance for first time in AWS Console 
--->To launch an EC2 instance for a web server, configure the AMI to define the operating system and software; select the instance type to allocate CPU, memory, and storage; and set up storage options, including the type and size of the volume.

Load balancing, permissions, and instance termination behavior are not required when launching a basic Amazon EC2 web server.

All interactions with services are powered by APIs. You can access these APIs through three primary methods: the AWS Management Console, the AWS CLI, or the AWS SDK. Let's review these methods.

![image](https://github.com/user-attachments/assets/4624da19-fe28-4727-93c4-7730957930c5)

The AWS Management Console is a web interface for managing AWS services, offering quick access to services, search functionality, and simplified workflows. With the mobile app, you monitor resources, view alarms, and check billing, supporting multiple logged-in identities at once.
Good for: Users who prefer a visual, easy-to-use interface for managing and configuring AWS services

With the AWS CLI, you manage multiple AWS services directly from the command line across Windows, macOS, and Linux. You can automate tasks through scripts, such as launching EC2 instances.
Good for: Advanced users and developers who need to automate tasks, script actions, and manage AWS resources efficiently from the command line

The AWS SDK simplifies integrating AWS services into your applications by providing APIs for various programming languages. AWS offers documentation and sample code for languages like C++, Java, and .NET to help you get started.
Good for: Developers looking to integrate AWS services into their applications using language-specific APIs

The AWS CLI enables automation through scripting, which is more efficient and reduces manual errors compared to the console.

The customer handles the operating system, networking, and applications on the EC2 instances. AWS manages the hardware.


---> Compute and shared responsibility

The AWS Shared Responsibility Model outlines the division of duties between the customer and AWS. AWS handles the security of the cloud (hardware and infrastructure), whereas the customer is responsible for security in the cloud (applications, data, and access control).


---> Amazon Machine Images:

An AMI includes the operating system, storage setup, architecture type, permissions for launching, and any extra software that is already installed. You can use one AMI to launch several EC2 instances that all have the same setup.

An AMI is a pre-configured virtual machine image that contains the operating system, application server, and applications. This helps to launch EC2 instances quickly with the desired software and settings.

![image](https://github.com/user-attachments/assets/a886ca5c-018c-4435-a85d-e61910b87c32)

--->  Three ways to use AMIs
First, you can create your own by building a custom AMI with specific configurations and software tailored to your needs. Second, you can use pre-configured AWS AMIs, which are set up for common operating systems and software. 
Lastly, you can purchase AMIs from the AWS Marketplace, where third-party vendors offer specialized software designed for specific use cases.

![image](https://github.com/user-attachments/assets/ff844107-e1e6-4a86-be79-a77b9f21238e)

-->  AWS pricing options

On-Demand Instances:
Pay only for the compute capacity you consume with no upfront payments or long-term commitments required.

Reserved Instances:
Get a savings of up to 75 percent by committing to a 1-year or 3-year term for predictable workloads using specific instance families and AWS Regions.

Spot Instances:
Bid on spare compute capacity at up to 90 percent off the On-Demand price, with the flexibility to be interrupted when AWS reclaims the instance.

Savings Plans:
Save up to 72 percent across a variety of instance types and services by committing to a consistent usage level for 1 or 3 years.

Dedicated Hosts:
Reserve an entire physical server for your exclusive use. This option offers full control and is ideal for workloads with strict security or licensing needs.

Dedicated Instances:
Pay for instances running on hardware dedicated solely to your account. This option provides isolation from other AWS customers.





## Resources:
- AWS documentation
- AWS Skill builder (course enrolled)
  
