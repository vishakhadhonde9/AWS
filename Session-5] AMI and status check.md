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
