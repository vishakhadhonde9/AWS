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

# Storage Classes in S3




