# AWS Basics for Beginners

## 1. Cloud Computing
Cloud computing is the on-demand delivery of IT resources (like servers, storage, databases, and networking) over the internet. Instead of purchasing and maintaining expensive hardware, businesses can rent these services from cloud providers like AWS. It follows a **pay-as-you-go** model, meaning users only pay for what they use. This approach reduces costs, improves flexibility, and enhances scalability.

---

## 2. Regions & Availability Zones (AZs)
AWS operates in different **Regions** worldwide, each containing multiple **Availability Zones (AZs)**. A **Region** is a physical location containing multiple **AZs**, and each AZ consists of one or more isolated data centers. This architecture ensures **high availability and disaster recovery** because if one AZ fails, AWS can automatically switch to another.

### Example:
- **Region:** US-East-1 (Virginia)
- **Availability Zones:** us-east-1a, us-east-1b, us-east-1c

This setup ensures **redundancy**, minimizing downtime and data loss.

---

## 3. Elastic Compute Cloud (EC2)
EC2 is AWS’s **virtual server** service that allows users to run applications in the cloud. Instead of maintaining physical servers, you can launch EC2 instances with the desired **CPU, RAM, storage, and operating system (Linux/Windows)**.

### Features:
- **Scalable** – Easily increase or decrease the number of servers as needed.
- **Flexible** – Choose different instance types optimized for computing, memory, or storage.
- **Secure** – Can be placed inside a **VPC** with firewall rules.

### Use Case:
Hosting websites, applications, or machine learning models.

---

## 4. Simple Storage Service (S3)
S3 is AWS’s **object storage** service that allows users to store and retrieve files, images, backups, and even static websites.

### Features:
- **Highly Scalable** – Can store unlimited data.
- **Durable & Reliable** – Data is automatically replicated across multiple AZs.
- **Secure** – Supports encryption and access control with IAM.

### Use Case:
Storing application data, backups, images, videos, and logs.

---

## 5. Amazon RDS (Relational Database Service)
RDS is a **fully managed** relational database service that supports **MySQL, PostgreSQL, MariaDB, SQL Server, and Oracle**. Instead of manually setting up and maintaining databases, AWS manages backups, patching, and scaling for you.

### Features:
- **Automated Backups** – Prevents data loss.
- **Scalability** – Can increase database size and performance automatically.
- **Multi-AZ Deployment** – Ensures high availability by replicating data across multiple AZs.

### Use Case:
Running applications that require structured data storage, such as e-commerce platforms, banking systems, and CRM applications.

---

## 6. AWS Lambda
AWS Lambda is a **serverless** computing service that runs your code in response to events without provisioning or managing servers.

### Features:
- **No Servers Needed** – AWS handles infrastructure and scaling.
- **Pay Per Execution** – You are only charged when your function runs.
- **Event-Driven** – Can be triggered by S3 uploads, API requests, or database changes.

### Use Case:
Running backend logic, processing S3 file uploads, automating tasks, and integrating with APIs.

---

## 7. Virtual Private Cloud (VPC)
A **VPC** is a **private network** within AWS that gives you control over network settings, including **IP addresses, subnets, security groups, and routing tables**.

### Features:
- **Customizable Networking** – Define your own network architecture.
- **Secure** – Uses firewalls, security groups, and access controls.
- **Connect to On-Premise Data Centers** – Using **VPN or Direct Connect**.

### Use Case:
Creating a secure and isolated environment for running applications and databases.

---

## 8. IAM (Identity and Access Management)
IAM helps manage **user permissions and security policies** in AWS. Instead of giving every user full access, you can create roles and policies to **restrict access based on job roles**.

### Features:
- **Granular Access Control** – Grant users only the necessary permissions.
- **Multi-Factor Authentication (MFA)** – Adds an extra layer of security.
- **Role-Based Access Control** – Assign permissions to users, groups, and applications.

### Use Case:
Restricting developers from accessing billing information while allowing them to manage EC2 and S3.

---

## 9. CloudWatch
CloudWatch is a **monitoring and logging service** that tracks AWS resources and applications. It helps users detect performance issues, security threats, and failures.

### Features:
- **Real-Time Monitoring** – Collects and visualizes metrics like CPU usage, memory, and network traffic.
- **Automated Alerts** – Sends notifications when thresholds are breached.
- **Log Management** – Stores application logs for debugging.

### Use Case:
Monitoring EC2 instance performance, tracking failed login attempts, and analyzing server logs.

---

## 10. Elastic Load Balancer (ELB)
ELB automatically distributes **incoming traffic across multiple servers** to improve availability and fault tolerance.

### Types of Load Balancers:
1. **Application Load Balancer (ALB)** – Routes traffic based on HTTP/HTTPS requests.
2. **Network Load Balancer (NLB)** – Routes traffic based on high-performance TCP connections.
3. **Classic Load Balancer (CLB)** – Basic traffic distribution (legacy).

### Features:
- **Prevents Downtime** – If one server fails, ELB redirects traffic to healthy servers.
- **Auto-Scalability** – Works with **Auto Scaling** to handle traffic spikes.
- **Secure** – Can terminate **SSL/TLS** connections for encrypted traffic.

### Use Case:
Balancing traffic for a website hosted on multiple EC2 instances.

---

## Summary
AWS provides **scalable, secure, and cost-effective** cloud computing services for businesses of all sizes. Understanding these core concepts will help you get started with cloud infrastructure.

