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
  
