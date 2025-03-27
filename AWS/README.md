# AWS Interview Questions and Answers

## 🔎 Basic Level AWS Questions

### What is AWS?
AWS (Amazon Web Services) is a leading cloud computing platform offering on-demand infrastructure, storage, and services globally. It provides scalable, reliable, and cost-effective solutions for enterprises, startups, and individuals.

👉 **Real-World Insight**: Enterprises leverage AWS to reduce capital expenses (CapEx) and shift to operational expenses (OpEx).

### What is EC2?
Amazon EC2 (Elastic Compute Cloud) provides scalable virtual servers in the cloud, allowing users to run applications without investing in physical hardware.

👉 **Use Case**: Hosting web applications, machine learning models, or microservices with auto-scaling capabilities.

### What is S3?
Amazon S3 (Simple Storage Service) is an object storage service designed for high availability and durability, used for storing and retrieving data anytime.

👉 **Use Case**: Data lakes, backups, and serving static website content.

### What is IAM?
AWS IAM (Identity and Access Management) enables secure access control by defining user permissions and policies.

👉 **Security Best Practice**: Use IAM roles over access keys and enforce MFA (Multi-Factor Authentication).

### What is VPC?
Amazon VPC (Virtual Private Cloud) allows you to define a logically isolated section of AWS to deploy resources securely.

👉 **Use Case**: Creating private subnets for secure backend services like databases.

### What is a Security Group?
A security group acts as a virtual firewall controlling inbound and outbound traffic for EC2 instances.

👉 **Best Practice**: Implement least privilege access—allow only necessary ports and protocols.

### What are Availability Zones (AZs)?
AWS AZs are physically separate data centers within a region that provide redundancy and fault tolerance.

👉 **Use Case**: Deploying applications across multiple AZs ensures high availability and disaster recovery.

## 🧑‍💻 Intermediate Level AWS Questions

### S3 vs. EBS: Key Differences?
| Feature     | S3                 | EBS                      |
|------------|--------------------|--------------------------|
| Type       | Object Storage     | Block Storage           |
| Use Case   | Data backup, file storage | Persistent storage for EC2 |
| Availability | Globally accessible | Tied to a specific AZ  |
| Performance | Higher latency    | Low latency            |

👉 **Best Practice**: Use S3 for data archiving and EBS for active workloads.

### What is Auto Scaling, and how does it work?
Auto Scaling automatically adjusts the number of EC2 instances based on demand to maintain performance and cost efficiency.

👉 **Real-World Example**: E-commerce sites scale up during Black Friday and scale down afterward.

### Instance Store vs. EBS?
- **Instance Store**: Temporary, high-speed storage attached to EC2 (data lost on instance stop).
- **EBS**: Persistent block storage attached to EC2, survives reboots.

👉 **Use Case**: Use instance store for caching and EBS for databases.

### What is CloudFront, and when would you use it?
AWS CloudFront is a CDN (Content Delivery Network) that caches content at edge locations for faster delivery.

👉 **Use Case**: Speeding up global website access by caching static files.

### ELB vs. CLB: What’s the Difference?
- **CLB (Classic Load Balancer)**: Basic load balancing for HTTP, HTTPS, TCP.
- **ELB (Elastic Load Balancer)**: Includes ALB (Application LB) and NLB (Network LB) for advanced routing.

👉 **Best Practice**: Use ALB for web apps, NLB for high-throughput applications.

### How does AWS Lambda work, and what are its use cases?
AWS Lambda is a serverless compute service that runs code in response to events without provisioning servers.

👉 **Use Case**: Triggering backend processing after an S3 file upload.

### Explain public and private subnets in a VPC.
- **Public Subnet**: Connected to the internet via an Internet Gateway (IGW).
- **Private Subnet**: No direct internet access, often uses a NAT Gateway.

👉 **Best Practice**: Host databases in private subnets for security.

### Compare Amazon RDS and DynamoDB.
| Feature    | RDS                  | DynamoDB                |
|------------|----------------------|--------------------------|
| Type       | Relational (SQL)      | NoSQL                    |
| Scalability | Vertical (limited auto-scaling) | Horizontal (fully managed scaling) |
| Use Case   | Structured, transactional data | High-speed, flexible schema data |

👉 **Use Case**: Use RDS for financial applications, DynamoDB for real-time gaming.

### What is an S3 bucket policy, and how is it used?
An S3 bucket policy defines permissions for objects within an S3 bucket, enabling secure access.

👉 **Best Practice**: Use least privilege access and enable encryption.

## 🚀 Advanced Level AWS Questions

### How does AWS CloudFormation automate infrastructure management?
AWS CloudFormation uses Infrastructure as Code (IaC) to define and provision AWS resources through templates.

👉 **Use Case**: Automating multi-region deployments with version control.

### What are the advantages of using AWS Organizations?
AWS Organizations help manage multiple AWS accounts with consolidated billing and security policies.

👉 **Best Practice**: Use Service Control Policies (SCPs) to enforce security across accounts.

### Explain the working of Amazon Route 53.
Route 53 is a scalable DNS (Domain Name System) service for routing traffic globally.

👉 **Use Case**: Configuring failover routing between multiple AWS regions.

### AWS Kinesis vs. AWS Lambda: What’s the Difference?
| Feature     | Kinesis            | Lambda                 |
|------------|--------------------|--------------------------|
| Type       | Real-time streaming | Event-driven compute    |
| Data Processing | Continuous    | Trigger-based           |
| Use Case   | Log analytics, IoT  | Automated workflows, API triggers |

👉 **Use Case**: Kinesis for real-time analytics, Lambda for event-driven tasks.

### What is AWS Elastic Beanstalk, and when should you use it?
Elastic Beanstalk automates application deployment without manual infrastructure management.

👉 **Use Case**: Deploying web applications quickly without deep AWS knowledge.

### Different Types of EBS Volumes & Use Cases?
- **gp3**: General-purpose, cost-effective.
- **io2**: High-performance for databases.
- **sc1**: Cold storage, infrequent access.

👉 **Best Practice**: Use gp3 for standard workloads, io2 for high IOPS.

### What is AWS Direct Connect, and why would you need it?
AWS Direct Connect establishes a private network connection between on-premise data centers and AWS.

👉 **Use Case**: Reducing latency for hybrid cloud setups.

### Use Cases of Amazon Elastic File System (EFS)?
EFS provides scalable, shared file storage for Linux workloads.

👉 **Use Case**: Centralized storage for multiple EC2 instances.

### What is AWS Trusted Advisor, and how can it optimize your environment?
AWS Trusted Advisor provides best practice recommendations for cost savings, security, and performance.

👉 **Best Practice**: Regularly review Trusted Advisor insights to optimize AWS usage.

### Walk me through the AWS Well-Architected Framework and its pillars.
The Well-Architected Framework consists of five pillars:
1. **Operational Excellence** – Monitoring and automation.
2. **Security** – Identity management, encryption.
3. **Reliability** – Fault tolerance, backups.
4. **Performance Efficiency** – Optimized resources.
5. **Cost Optimization** – Eliminating waste.
