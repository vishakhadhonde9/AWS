# EBS Snapshot-
- EBS Snapshot is backup of EC2 attached EBS volume.
- Snapshots capture the state of your volume at a specific point in time.
- Snapshots can be used for disaster recovery, migrating data across regions and accounts.
- EBS snapshots are incremental backups that only save the blocks on the volume that have changed after your most recent snapshot.

# EBS Volume Encryption-
- When a volume is encrypted, all data stored on it is encrypted, including the boot and data volumes.
- When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted:
   - Data at rest inside the volume.
   - All data moving between the volume and the instance.
   - All snapshots created from the volume.
   - All volumes created from those snapshots
 # Pricing-
 - Volume storage for all EBS volume types is charged by the amount of GB you provision per month until you release the storage.
 - Costs increase for EBS volumes that support additional input/output operations per second (IOPS) and throughput beyond baseline performance.
 - Amazon EBS calculates charges for snapshots by the gigabyte-month. You incur charges based on the size of your snapshot and the length of time that you keep the snapshot.
 - AWS Free Tier includes 30 GB of storage, 2 million I/Os, and 1 GB of snapshot storage with Amazon Elastic Block Store (EBS).
  
# EBS Volume Management-

## Partitions-
- Partitioning is the process of dividing a storage device, like a hard drive or SSD, into multiple logical sections or partitions.
- Each partition acts as a separate storage unit, allowing you to organize data, install multiple operating systems, or separate system files from user files.
- **Mounting Partitions-** To access and use the data on a specific partition, you need to "mount" it. This involves attaching the partition to a directory in the file system hierarchy of the operating system.
- **Mount Point-** When you mount a partition, you attach it to a specific directory, so that you can access and manage the files stored on that partition.
- **UUID (Universally Unique Identifier)-** 128-bit number used to uniquely identify an object or entity, such as a storage device or partition.
- UUID (Universally Unique Identifier) is a unique value assigned to storage devices and partitions, which ensures that each device or partition can be uniquely identified and reliably accessed across reboots and changes in device names.

### Partitioning Process-
- After attaching an EBS volume to an EC2 instance, you typically need to create partitions, create a file system, mount the partitions, and ensure they mount automatically on reboot. 

1. Creating Partitions

              1. Attach the EBS Volume:
                 - Attach your EBS volume to your EC2 instance using the AWS Management Console, AWS CLI.
                 - Note the device name (e.g., `/dev/xvdf`).
              
              2. Identify the Device:
               
                 lsblk
                 - This command lists all available block devices. Identify your newly attached EBS volume.
              
              3. Create Partitions using `fdisk`:
                 fdisk command is used to create, modify and delete partitions.
               
                    sudo fdisk /dev/xvdf
          
                 - n-create new partitions
                 - d-delete partitions
                 - p-print partition table
                 - w-write changed and exit
                 - q-quit
   
                 - Follow the steps:
                   - Press `n` to create a new partition.
                   - Select `p` for primary partition.
                   - Choose the partition number (usually `1` for the first partition).
                   - Accept the default first sector.
                   - Accept the default last sector or specify a size.
                   - Press `w` to write the partition table and exit.
              
              4. Verify the Partition:
              
                 lsblk
                 - The new partition should appear as `/dev/xvdf1`.


3. Creating a File System

                  1. Create a File System:
                     - to create an ext4 file system:
                       sudo mkfs.ext4 /dev/xvdf1
                      
                     - Other file systems:
                       - XFS: `sudo mkfs.xfs /dev/xvdf1`
                       - EXT3: `sudo mkfs.ext3 /dev/xvdf1`

4. Mounting Partitions

                  1. Create a Mount Point:
                     sudo mkdir /mnt/mydata
                  
                  
                  2. Mount the Partition:
                     sudo mount /dev/xvdf1 /mnt/mydata
                  
                  3. Verify the Mount:
                     df -h
                     - This command shows the mounted file systems. Verify that `/dev/xvdf1` is mounted to `/mnt/mydata`.

5. Permanent Mount Configuration
   
        To ensure the partition mounts automatically after a reboot, update the `/etc/fstab` file.

                  1. Get the UUID of the Partition:
                   
                     sudo blkid /dev/xvdf1
                     - Copy the UUID from the output.
                  
                  2. Edit `/etc/fstab`:
                     sudo vi /etc/fstab
                  - Add an entry for the new partition. Use the UUID from the previous step. For example:
                    
                       UUID=your-uuid-here /mnt/mydata ext4 defaults,nofail 0 2
                      
                  - Replace `your-uuid-here` with the actual UUID and adjust the file system type if 
                        necessary.








