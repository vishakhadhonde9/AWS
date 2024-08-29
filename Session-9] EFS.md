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




