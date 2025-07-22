# Amazon Machine Image-
- An Amazon Machine Image (AMI) is an image provided by AWS that provides the information required to launch an instance.
- An Amazon Machine Image (AMI) is a pre-configured template that you use to create EC2 instances.
- It contains the information required to launch an instance, such as the operating system, application server, and applications.
- An AMI is composed of the following components:
    - Root volume template: This is the primary storage for the instance, containing the operating system and other pre-installed software.
    - Launch permissions: These define who can use the AMI to launch instances.
    - Block device mappings: These specify the additional storage volumes (EBS volumes) to be attached to the instance at launch time

# Types of AMI- 
## 1] Amazon-provided AMIs: 
- These are pre-configured by Amazon with popular operating systems like Linux or Windows, ready to use immediately.

## 2] Marketplace AMIs: 
- These are created by third-party vendors and available for purchase or subscription on the AWS Marketplace.
- They often come with pre-installed software.

## 3] Community AMIs: 
- These are shared by other AWS users.
- They can be free to use and are typically configured to meet specific community needs or preferences.

## 4] Custom AMIs: 
- These are created by you or your organization. 
- They are tailored to meet your specific requirements, including custom software configurations, settings, and applications.

# Status Check-
- In Amazon EC2, status checks monitor the health of your instances.
- Amazon EC2 performs these checks automatically and reports their results to help you identify issues.
- Amazon EC2 performs automated checks on every running EC2 instance to identify hardware and software issues.
- You can view the results of these status checks to identify specific and detectable problems.
- There are three types of status checks:
     - System status checks
     - Instance status checks
     - Attached EBS status checks

## 1] System Status Check-
- System status checks monitor the AWS systems on which your instance runs.
- These checks detect underlying problems with your instance that require AWS involvement to repair.
- When a system status check fails, you can choose to wait for AWS to fix the issue, or you can resolve it yourself.
- These checks ensure the physical machine (hardware) hosting your instance is working correctly. It as a health check for the underlying infrastructure provided by AWS.
- The following are examples of problems that can cause system status checks to fail:
     - Loss of network connectivity
     - Loss of system power
     - Software issues on the physical host
     - Hardware issues on the physical host that impact network reachability
- If a system status check fails, we increment the StatusCheckFailed_System metric.


## 2] Instance status checks-
- Instance status checks monitor the software and network configuration of your individual instance.
- These checks ensure that your specific EC2 instance is healthy and running correctly. It's like a health check for the virtual machine you control.
- The following are examples of problems that can cause instance status checks to fail:
      - Failed system status checks
      - Incorrect networking or startup configuration
      - Exhausted memory
      - Corrupted file system
      - Incompatible kernel
- If an instance status check fails, we increment the StatusCheckFailed_Instance metric.

## 3] Attached EBS status checks-
- Attached EBS status checks are a crucial aspect of monitoring your EC2 instances.
- They ensure that the Amazon EBS (Elastic Block Store) volumes attached to your instances are functioning correctly and able to perform input/output (I/O) operations.
- The following are examples of issues that can cause attached EBS status checks to fail:
      - Hardware or software issues on the storage subsystems underlying the EBS volumes
      - Hardware issues on the physical host that impact reachability of the EBS volume.
      - Connectivity issues between the instance and EBS volumes
- The StatusCheckFailed_AttachedEBS metric that indicates impairment if one or more of the EBS volumes attached to the instance are unable to complete I/O operations. 


# Launch Template-
- You can use a launch template to store instance launch parameters so that you do not have to specify them every time you launch an instance.
- It includes details like the instance type, AMI (Amazon Machine Image), storage options, and any configuration settings you want to apply.
- When you want to launch new instances, you use the launch template to automatically apply all those settings, saving time and ensuring consistency.









