# Elastic File System (Amazon EFS)-
- EFS is a scalable file storage service offered by AWS.
- Amazon Elastic File System (Amazon EFS) is a set-and-forget(minimum management) file system that automatically grows and shrinks as you add and remove files.
- It can be accessed by multiple EC2 instances concurrently.
- EFS can be accessed across multiple Availability Zones within a region.


# Storage Classes in EFS-
- **1] Standard storage class-**
  - This is the default storage class for EFS.
  - The user is only charged for the amount of storage used.
  - This is recommended for storing frequently accessed files.**

- **2] Infrequently Accessed storage class(One Zone)-**
  - Cheaper storage space.
  - Recommended for rarely accessed files.
  - Increased latency when reading or writing files.
  - The user is charged not only for the storage of files but also charged for read and write operations.

# Network File System(NFS)-
- Network File System (NFS) is a distributed file system protocol that allows users to access files over a network.
- Elastic File System (EFS) primarily uses the NFS (Network File System) protocol.
  

# EBS VS EFS-
| **Attribute**          | **Block Storage (e.g., Amazon EBS)**                             | **File Storage (e.g., Amazon EFS)**                                    |
|------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------------|
| **Accessibility**      | Single EC2 instance                   | Multiple EC2 instances across multiple AZs                           |
| **Scalability**        | Predefined size (must manually increase)                         | Automatically scales based on storage usage                           |
| **Performance Modes**  | Provisioned IOPS, General Purpose                                | General Purpose, Max I/O                                             |
| **Throughput Modes**   | Determined by volume size and type                               | Bursting, Provisioned                                                 |
| **Data Persistence**   | Persistent within the AZ                                         | Persistent across multiple AZs                                        |

# Steps-
1. Launch two EC2 instances in the same VPC and subnet. Use Amazon Linux 2 AMI.
2. Attach role to EC2 instance with amazonefsfullaccess permission.

3. create an EFS File System

4. Install NFS Client on EC2 Instances
   - SSH into each EC2 instance.
   - Install the NFS client using the following commands:
   
             sudo yum -y update
             sudo yum -y install nfs-utils

5. Mount the EFS File System
   - Create a directory to mount the EFS:
     sudo mkdir /mnt/efs

   - Mount the EFS file system:
     sudo mount -t nfs4 -o nfsvers=4.1 <EFS_DNS_Name>:/ /mnt/efs
 
   - Verify the mount:
     df -h
6. Test the File System
   - Create a test file:
     echo "Hello EFS" | sudo tee /mnt/efs/hello.txt
    
   - Verify the file is accessible from both EC2 instances:
      cat /mnt/efs/hello.txt
     

 Cleanup

- Unmount the EFS file system:
  sudo umount /mnt/efs
 
- Terminate the EC2 instances.
- Delete the EFS file system from the console.

   
