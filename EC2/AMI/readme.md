# AWS AMI (Amazon Machine Image)

## **What is AWS AMI?**

An **Amazon Machine Image (AMI)** is a pre-configured template that provides the necessary information to launch an EC2 instance in AWS.

It acts as a blueprint for creating EC2 instances with the required operating system, software, and configurations already installed.

---

## **AMI Includes**

- **Operating System** (e.g., Linux, Windows)
- **Application Server** (e.g., Apache, Nginx)
- **Pre-installed Software and Configurations**

---

## **Why Use an AMI?**

- Launch EC2 instances quickly.
- Create multiple identical instances.
- Maintain consistent environments across deployments.
- Simplify backup, migration, and disaster recovery.

---

## **Launch Template vs AMI**

| **Feature** | **Create Launch Template** | **Create Image (AMI)** |
|--------------|----------------------------|-------------------------|
| **Purpose** | Create a reusable blueprint for launching instances | Create a custom AMI snapshot of an instance |
| **Content** | Contains configuration settings (e.g., AMI, instance type, security groups, etc.) | Captures OS, applications, configurations, and data |
| **Reusability** | Used repeatedly to launch new instances in a consistent way | Used to create new instances that replicate the captured image |
| **Use Cases** | Auto Scaling, Spot Instances, Standardizing instance settings | Backup, Replication, Migrating instances to another region |
| **Versioning** | Can have multiple versions for different configurations | Typically, an AMI is a point-in-time capture of an instance |

---

## **Key Difference**

### **Launch Template**
- Stores **instance configuration**.
- Used to launch EC2 instances with consistent settings.
- Supports versioning.
- Commonly used with **Auto Scaling Groups** and **Spot Instances**.

### **Amazon Machine Image (AMI)**
- Stores the **entire machine image**, including the operating system, applications, configurations, and data.
- Used to create identical EC2 instances.
- Acts as a snapshot of an existing instance.
- Commonly used for **backup**, **migration**, and **disaster recovery**.