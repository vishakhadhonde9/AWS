# Elastic Block Storage-
- EBS provides **block-level** storage service that can use provided storage volumes in Amazon EC2 instances.
- Each volume acts like a hard drive, offering storage that remains available.
- EBS Volumes are persistent in nature means even if you stop or terminated the instance the storage remains availble.
- Can attaches to single EC2 at time.
- Both EBS Volume and EC2 will be in same AZ.

# Types of EBS Volume-
- **1] Solid State Drive-**
- **2] Hard Disk Drive-**
- **3] Magnetic Standard-**


## Solid State Drive(SSD)-
- SSD-backed volumes are optimized for IOPS, which are best for workloads involving frequent read/write operations with small I/O size.
- SSD is bootable drive
- SSD have two types-

### 1] General Purpose SSD-
- It is default EBS voulme type for EC2 instance.
- offer a balance of price and performance for a variety of workloads. 
- It can be of two types:
- **GP2-**
     - Highly recomended as boot volumes for EC2.
     - can be range in 1 GiB to 16 TiB
- **GP3-**
     -  Default EBS volume types for EC2.
     -  The most recent generation of SSD general purpose volumes are referred to as gp3 volumes.
     -   At a cheaper cost than gp2.

### 2] Provisioned IOPS SSD-
- Privisioned IOPS SSD are designed to meet the needs of I/O intensive workloads, particularly database workloads.
- can range in size from 4 GiB to 16 TiB.
- It can be of three types: io1, io2 and io2 block express.

# 2] Hard Disk Drive-
- Hard Disk Drives are usually preferred in cases where high Throughput is required during a large and sequential I/O operation such as reading video files, logs processing, etc.
- HDDs are cheaper compared to SSDs and ideal for tasks that require high throughput.
- HDD is not  bootable.
- It can be of two types: Throughput Optimized HDD and Cold HDD.
- **Throughput Optimized HDD (st1)-**
      - It provide high throughput for accessing large and sequential data and support frequently accessed storage requirements.
- **Cold HDD (sc1)-**
      - Designed for less frequently accesses workloads but higher throughput.

# 3] Magnetic Standard-
- Magnetic (standard) volumes are previous generation volumes.
- They are suited for workloads with small datasets where data is accessed infrequently and performance is not of primary importance.

| **Attribute**                | **Magnetic EBS Volume**                  |
|------------------------------|------------------------------------------|
| **Volume Size**              | 1 GiB – 1 TiB                           |
| **Maximum IOPS per Volume**  | 40 – 200 IOPS                            |
| **Maximum Throughput per Volume** | 40 – 90 MiB/s                        |
| **Boot Volume**              | Supported                                |
| **Multi-Attached Volumes**   | Not supported                            |
| **Latency**                  | Higher latency compared to SSDs and HDDs|
| **Price**                    | Lower cost compared to SSDs and HDDs    |




| **Attribute**                | **General Purpose SSD (gp3)** | **General Purpose SSD (gp2)** | **Provisioned IOPS SSD (io2)** | **Provisioned IOPS SSD (io1)** | **Provisioned IOPS SSD (io2 Block Express)** | **Throughput Optimized HDD (st1)** | **Cold HDD (sc1)** |
|------------------------------|------------------------------|------------------------------|-------------------------------|-------------------------------|-----------------------------------------|-----------------------------------|--------------------|
| **Volume Size**              | 1 GiB – 16TiB               | 1 GiB – 16 TiB               | 4 GiB – 16 TiB                | 4 GiB – 16 TiB                | 4 GiB – 64 TiB                         | 500 GiB – 16 TiB                   | 500 GiB – 16 TiB   |
| **Minimum IOPS**             | 100 IOPS                     | 3000 IOPS                     | 100 IOPS                      | 100 IOPS                      | 100 IOPS                                | 100 IOPS                           | 50 IOPS            |
| **Maximum IOPS**             | 16,000 IOPS                  | 16,000 IOPS                  | 64,000 IOPS                   | 64,000 IOPS                   | 256,000 IOPS                            | 500 IOPS                           | 250 IOPS           |
| **Maximum Throughput**       | Up to 1,000 MB/s             | Up to 250 MB/s               | Up to 1,000 MB/s              | Up to 500 MB/s                | Up to 4,000 MB/s                        | Up to 500 MB/s                     | Up to 250 MB/s     |
| **Boot Volume**              | Supported                    | Supported                    | Supported                     | Supported                     | Supported                               | Supported                          | Supported          |
| **Multi-Attached Volumes**   | Supported                    | Not supported                | Not supported                 | Not supported                 | Not supported                           | Not supported                      | Not supported      |
| **Latency**                  | Single-digit milliseconds    | Single-digit milliseconds    | Single-digit milliseconds     | Single-digit milliseconds     | Single-digit milliseconds               | Single-digit milliseconds          | Single-digit milliseconds |







                                                                                       
