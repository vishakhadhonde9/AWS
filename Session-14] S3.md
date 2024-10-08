# Simple Storage Service (S3)-
- S3 is a highly scalable and durable object storage service offered by AWS.
- It is designed to store and retrieve any amount of data, at any time, from anywhere.
- It stores different types of data like Photos, Audio, and Videos as Objects.

## Bucket-
- To upload your data (photos, videos, documents, etc.) to Amazon S3, you must first create an S3 bucket.
- A bucket is a container for objects stored in Amazon S3 where u can store your data.
- You can store any number of objects in a bucket and can have up to 100 buckets in your account.

#### Rules for Bucket Creation-
- Bucket names must be globally unique across all of AWS. No two buckets can have the same name.
- Must be between 3 and 63 characters long.
- Can only contain lowercase letters, numbers, hyphens (-), and periods (.).
- Must start and end with a lowercase letter or number.
- Should not be formatted as IP addresses (e.g., 192.168.1.1).
- A bucket has no limit to the amount of objects that it can store. No bucket can exist inside of other buckets.
- You can create up to 100 buckets in each of your AWS cloud accounts, with no limit on the number of objects you can store in a bucket.

## Object-
- Objects are the entities which are stored in an S3 bucket.
- An object consists of object data and metadata where metadata is a set of name-value pair that describes the data.
- An object consists of some default metadata such as date last modified, and standard HTTP metadata, such as Content type. 
- It is uniquely identified within a bucket by key and version ID.
- The maximum size of an object in an Amazon S3 bucket is 5 terabytes (TB).
#### Key-
- A key is a unique identifier for an object.
- Every object in a bucket is associated with one key.

# Versioning in S3-
- Versioning in Amazon S3 is a means of keeping multiple variations of an object in the same bucket.
- You can use the S3 Versioning feature to preserve, retrieve, and restore every version of every object stored in your buckets.
- Versioning-enabled buckets can help you recover objects from accidental deletion or overwrite.
- When you delete an object in a versioned bucket, S3 does not permanently remove the object. Instead, it creates a "delete marker" that becomes the current version. The actual object still exists and can be restored if needed.

# Storage Classes in S3-
- Amazon S3 offers various storage classes to help you manage your data efficiently based on your access patterns, cost requirements, and durability needs.

## Standard Storage Class- 
  - It is used for general purposes and offers high durability, availability, and           performance object storage for frequently accessed data.
  - S3 Standard is appropriate for a wide variety of use cases, including cloud             applications, dynamic websites, content distribution, mobile and gaming                 applications, and big data analytics.
  - Use Case: Frequently accessed data.
  - Durability: 99.999999999% (11 9’s) durability over a given year.
  - Availability: 99.99% availability over a given year.
  - Cost: Higher cost compared to other classes; best for frequently accessed data where low latency is critical.

## S3 Standard-Infrequent Access-
  - To access the less frequently used data, users use S3 Standard-IA. It requires           rapid access when needed.
  - It is best in storing the backup, and recovery of data for a long time. It act as a     data store for disaster recovery files.
  - Use Case: Data that is accessed less frequently but needs to be rapidly accessible       when needed.
  - Durability: 99.999999999% (11 9’s) durability over a given year.
  - Availability: 99.9% availability over a given year
  - Cost: Lower storage cost compared to Standard, but with a retrieval charges.

## S3 One Zone-Infrequent Access-
  - S3 One Zone-IA stores data in a single Availability Zone and costs 20% less than S3     Standard-IA.
  - It’s a very good choice for storing secondary backup copies of on-premises data or      easily re-creatable data.
  - S3 One Zone-IA provides you the same high durability, high throughput, and low          latency as in S3 Standard.
  - Use Case: Infrequently accessed data that does not require multiple availability        zone resilience.
  - Durability: 99.999999999% (11 9’s) durability over a given year.
  - Availability: 99.5% availability over a given year.
  - Cost: Lower cost than Standard-IA as it is stored in a single availability zone.

#  S3 Intelligent-Tiering-
  - Automated Cost Optimization for Data with Unknown Access Patterns
  - The first cloud storage automatically decreases the user’s storage cost. It             provides very cost-effective access based on frequency, without affecting other         performances.
  - It also manages tough operations. Amazon S3 Intelligent – Tiering reduces the cost      of granular objects automatically.
  - No retrieval charges are there in Amazon S3 Intelligent – Tiering.
  - Use Case: Data with unknown or changing access patterns.
  - Durability: 99.999999999% (11 9’s) durability over a given year.
  - Availability: 99.9% availability over a given year.
  - Cost: Optimizes costs by automatically moving objects between two access tiers          (frequent and infrequent) based on changing access patterns.

# S3 Glacier-
  - It designed for long-term archival and infrequent access.
  - It provides low-cost storage with varying retrieval times based on your needs.
  - S3 Glacier is intended for data that is rarely accessed and needs to be retained        for long periods.
  - Use Case: Long-term archival storage with retrieval times ranging from minutes to       hours.
  - Durability: 99.999999999% (11 9’s) durability over a given year.
  - Availability: 99.99% availability over a given year.
  - Cost: Very low cost for storage; retrieval costs vary based on retrieval speed.

# Amazon S3 Glacier Deep Archive-
  - Amazon S3 Glacier Deep Archive is the lowest-cost storage class within Amazon S3,      specifically designed for long-term archival of data that is rarely accessed.
  - Use Case: Long-term archival of data that is rarely accessed, with retrieval times     of up to 12 hours.
  - Durability: 99.999999999% (11 9’s) durability over a given year.
  - Availability: 99.9% availability over a given year.
  - Cost: Lowest cost for long-term storage; higher retrieval costs.
