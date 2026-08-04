# AWS EBS (Elastic Block Store)

## **What is AWS EBS?**

AWS EBS is a cloud-based storage service that provides durable, high-performance block storage for use with Amazon EC2 instances.

It works like a virtual hard drive, allowing you to store and access data even when your EC2 instances are stopped or terminated.

---

## **Use Case**

For example, if you're hosting a MySQL or PostgreSQL database, you need reliable, high-performance storage to handle frequent read/write operations.

EBS provides persistent, fast storage that ensures your data is saved even if the EC2 instance is stopped or restarted, making it ideal for database workloads.

---

## **Important Points About EBS**

* Region & AZ specific.
* **Built-in Redundancy**

  * EBS volumes are automatically replicated within the same Availability Zone to prevent data loss due to hardware failures.
* **Different Volume Types**

  * `gp2`
  * `gp3`
  * `io1`
  * `io2`
  * `st1`
  * `sc1`
* Allows **Encryption** and **Snapshots** for backup.
* **Scalable** (Volume can be resized)

  * No data loss will occur during resizing.
  * No need to restart the EC2 instance during the process.
