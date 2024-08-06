# Elastic Compute Cloud (EC2)-
- Amazon EC2 is a web service that provides secure, resizable compute capacity in the cloud.
- **EC2 Instance:** is simply a virtual machine or virtual server.
- it offers flexible, scalable, and cost-effective computing power.
- It reduce hardware costs so you can deploy application faster.
- **Elastic-** we can easily increase or decrease no. of servers or size of exiting servers.
- **Compute-** allows to process data or to host an application.
- **Cloud-** it is service hosted in Cloud technology.

# Amazon Machine Image (AMI)-
- An Amazon Machine Image (AMI) is an image provided by AWS that provides the information required to launch an instance.
- An Amazon Machine Image (AMI) is a pre-configured template that you use to create EC2 instances.
- It contains the information required to launch an instance, such as the operating system, application server, and applications.
- You must specify an AMI when you launch an instance.
- You can launch multiple instances from a single AMI when you require multiple instances with the same configuration.
- You can use different AMIs to launch instances when you require instances with different configurations.

- An AMI includes the operating system, storage mapping, architecture type, launch permissions, and any additional preinstalled software applications.

# Types of Instances-
### Instance Notation:

![final_instance_ex](https://github.com/user-attachments/assets/47293aa1-d7ff-4fa6-bddd-7f59a95980b4)


## 1] General Purpose Instance-
- It provides a good range of computing, memory and networking resources and making them suitable for a wide variety of applications.
- These instances are useful for wide range of applications like web servers, executing codes, repositories that require such resources in equal parts.
- Examples: t2, t3, t4, m5 and m6 etc.


## 2] Compute Optimized Instance-
- Suitable for compute-intensive application that that require a lot of computation and help from high-performance CPUs.
- They prioritize CPU capabilities, but also offer balanced memory and networking to support their performance.
- This instance type is best suited for high-performance applications like web servers, Gaming servers.
- Examples: c4, c5 and c6 etc.
  
## 3] Memory Optimized Instance-
- provide high amounts of memory(RAM) relative to CPU resources. They are ideal for applications that require large amounts of memory to perform efficiently.
- They prioritize memory capacity and speed, providing more RAM compared to CPU resources.
- Useful for large databases and caching servers etc.
- Examples: R4, R5 and X1 etc.

## 4] Storage Optimized Instance-
- Designed for applications that need a lot of storage space and fast access to that storage.
- Storage-optimizeOffers large amounts of disk space to store big data, files, or applications.
- Offers large amounts of disk space to store big data, files, or applications.
- Useful for Log Processing, backup processing, etc.
- Examples: I3, D2, D3 and H1 etc.

## 5] Accelerated Optimized Instance-
- Specialized instances designed to handle tasks that benefit from additional hardware acceleration.
- It uses coprocessor or specialized hardware like GPUs (Graphics Processing Units).
- Useful for graphics processing, video processing and Machine Learning.
- Examples: F1, G4 and P4 etc.

# Key Pair-
- Key pair is a set of security credentials used to access your EC2 instances securely.
- Key pairs are used to securely connect to your EC2 instances without needing to enter a password. They help ensure that only authorized users can access your instances.
- **Key pair consist of:** Public key and Private key
### Public Key-
-  This key is like a lock that’s installed on your server.
-  It’s safe to share because it’s only used to keep the server secure.
### Private Key-
- You use the private key to authenticate and connect to your EC2 instance.
- The private key matches the public key on the instance, enabling a secure connection.
- You keep it private and secure; not shared with anyone. It allows you to open the server and access it.

# Security Group-
- It is act as firewall that control traffic to instance.
- It helps protect your server by specifying which types of network traffic are allowed to reach it.
#### Rules for Traffic:
    - Inbound Rules: Define what kind of incoming traffic (data coming into your server) is allowed. 
    - Outbound Rules: Define what kind of outgoing traffic (data going from your server) is allowed.
#### Access Control:

    - Allow or Block: Security groups can allow or block traffic based on rules you set. 
    For example, you can set a rule to allow access only from certain IP addresses or to block traffic from all sources except your own network.







