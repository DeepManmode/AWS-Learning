# AWS EC2 (Elastic Cloud Compute)

## **What is AWS EC2?**

AWS EC2 (Amazon Elastic Compute Cloud) is a cloud service that provides resizable virtual servers, called instances, which you can use to run applications.

## **Example**

Imagine you're running a business and need a server to host your website or application.

Instead of buying and managing physical servers, AWS EC2 lets you rent virtual servers in the cloud. These virtual servers are called instances.

---

## **Configure Several Options**

- **Instance Type:** Select the hardware capacity (e.g., CPU, memory).
- **AMI (Amazon Machine Image):** Choose the operating system and software (Linux, macOS, Windows).
- **Storage:** Configure the type and size of storage (e.g., EBS volume).
- **Security Groups:** Set up firewall rules to control inbound/outbound traffic.
- **Key Pair:** Create or use an existing key pair for SSH access.
- **Network Settings:** Configure VPC, subnet, and assign public or private IP addresses.
- **IAM Role:** Attach an IAM role for permissions to access other AWS resources.
- **User Data:** Add scripts to be executed when the instance starts.
- **Elastic IP:** Optionally associate a static IP address for consistent public access.

---

## **Instance Types**

### **Case 1: Small Website or Blog**

- **Suitable Type:** `t3.micro` or `t3.small` (General Purpose)

### **Case 2: E-Commerce Application**

- **Suitable Type:** `m5.large` or `m5.xlarge` (General Purpose)

### **Case 3: Real-Time Video Rendering and Streaming (Accelerated Computing)**

- **Suitable Type:** `g5.12xlarge` or `g5.24xlarge`

### **Case 4: In-Memory Database for Real-Time Analytics (Memory Optimized)**

- **Suitable Type:** `r6g.16xlarge` or `x2idn.32xlarge` (Memory Optimized)