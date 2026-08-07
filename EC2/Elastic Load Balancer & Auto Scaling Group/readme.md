# Elastic Load Balancer (ELB)

## **What is Elastic Load Balancer?**

An **Elastic Load Balancer (ELB)** distributes incoming application traffic across multiple EC2 instances to improve availability, scalability, and fault tolerance.

---

## **Key Features**

- **Distributes Traffic:** It splits incoming traffic across multiple servers so no single server gets overloaded.
- **Improves Availability:** If one server goes down, the load balancer automatically sends traffic to the working servers, ensuring your application stays available.
- **Scales Resources:** It helps manage high demand by adding more servers during peak times and distributing the load.
- **Single Point of Access:** Only one endpoint needs to be exposed to users.
- **High Availability (HA):** Works across multiple Availability Zones (AZs).

---

## **Types of AWS Load Balancers**

### **Application Load Balancer (ALB)**

- Perfect for web applications.
- Handles complex **HTTP** and **HTTPS** requests.
- Operates at **Layer 7 (Application Layer)**.

### **Network Load Balancer (NLB)**

- Designed for **high performance** and **low latency**.
- Handles **TCP/UDP** traffic.
- Suitable for applications such as **gaming** and **financial applications**.
- Operates at **Layer 4 (Transport Layer)**.

### **Gateway Load Balancer (GWLB)**

- Helps deploy, scale, and manage third-party virtual appliances.
- Commonly used for:
  - Firewalls
  - Monitoring solutions
  - Security appliances

---

# Auto Scaling Group (ASG)

## **What is Auto Scaling Group (ASG)?**

AWS ASG (Auto Scaling Group) is a service that automatically adds or removes EC2 instances based on demand to ensure your application is always available.

It helps scale up when more capacity is needed and scale down during low usage to save costs, keeping the right number of servers running at all times.

---

## **Functions of Auto Scaling Group**

- **Automatic Scaling:** Scale the number of EC2 instances up or down based on demand.
- **Maintain Instance Health:** Replace unhealthy instances automatically to ensure reliability.
- **Use Scaling Policies:** Set rules for scaling based on metrics like CPU usage or request count.
- **Ensure Availability:** Always keep a defined number of instances running to meet application needs.
- **Schedule Scaling:** Pre-configure scaling activities for specific times (e.g., traffic peaks).
- **Distribute Instances:** Deploy instances across multiple Availability Zones for high availability.
- **Integrate with ELB:** Attach instances to an Elastic Load Balancer to automatically balance traffic.
- **Optimize Costs:** Scale down during low demand to save on infrastructure costs.

# Scalability

## **What is Scalability?**

Scalability means the ability to grow your system's resources when your application or website gets more traffic or more users.

### **Example**

- Increase the number of EC2 instances to handle higher traffic.
- Upgrade resources to support more users and workloads.

---

# High Availability (HA)

## **What is High Availability?**

High Availability (HA) means keeping your service up and running with minimal downtime, so it's always accessible to users.

### **Example**

- Running resources across **multiple Availability Zones (AZs)** to ensure the application remains available even if one AZ fails.

---

# Elasticity

## **What is Elasticity?**

Elasticity means the ability to automatically adjust resources as the demand changes—adding more resources when needed and removing them when they're no longer necessary.

### **Example**

- **Auto Scaling Group (ASG)** automatically launches additional EC2 instances during high traffic and terminates them when demand decreases.