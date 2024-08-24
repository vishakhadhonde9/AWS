# Identity and Access Management (IAM)-
- It is a service that helps you or allows you securely control access to AWS services and resources
- It also provides a centralized view of who and what are allowed inside your AWS account (authentication), and who and what have permissions to use and work with your AWS resources (authorization).
- With IAM, you can manage permissions that control which AWS resources users can access using athorization and authentication.
- You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.
- IAM in AWS follows the Principle of **Least Privilege**.
- This principle is a security best practice that dictates that each user, group, or role should have only the permissions necessary to perform their specific tasks or functions.
- With IAM, you can share access to an AWS account and resources without sharing your set of access keys or password.
### Authentication-
- Authentication is the proving who you are at door.
- Authentication means confirming your identity, usually with username and password.
- Authentication confirms that users are who they say they are.
- User names and passwords are the most common types of authentication. But you might also work with other forms, such as token-based authentication or biometric data, like a fingerprint.
- Authentication simply answers the question, “Are you who you say you are?”

### Authorization-
- Authorization is the process of giving users permission to access AWS resources and services.
- Authorization determines whether a user can perform certain actions, such as read, edit, delete, or create resources.
- Authorization answers the question, “What actions can you perform?” 
  
# IAM User-
- IAM user is an entity that represents a person who needs to interact with AWS resources.
- You define the user in your AWS account.

# IAM Group-
- An IAM group is a collection of users.
- All users in the group inherit the permissions assigned to the group.
- This makes it possible to give permissions to multiple users at once.
- It’s a more convenient and scalable way of managing permissions for users in your AWS account.
- features of groups:
   - Groups can have many users.
   - Users can belong to many groups.
   - Groups cannot belong to groups.

# IAM policies-
- To manage access and provide permissions to AWS services and resources, you create IAM policies and attach them to an IAM identity.
- Whenever an IAM identity makes a request, AWS evaluates the policies associated with them.
- IAM policy is a JSON document that specifies permissions. It defines what actions are allowed or denied on resources.
- Policies can be attached to IAM users, groups, or roles to grant or restrict access.

## Types of policies-
# 1)AWS Managed Policies-
- These are predefined policies created and maintained by AWS.
- Examples- AmazonS3ReadOnlyAccess, AmazonEC2FullAccess etc.

# 2)Customer Managed Policies-
- These are policies created and managed by you (or your organization).
- They allow for more customization than AWS managed policies.
- Custom policies tailored to specific needs, like granting permissions only for certain S3 buckets or EC2 instances.

# 3)Inline Policies-
- An inline policy is a policy created for a single IAM identity (a user, user group, or role).
- Inline policies maintain a strict one-to-one relationship between a policy and an identity.
- They are deleted when you delete the identity.
- They are not reusable like managed policies.


# IAM Role-
- IAM Role is a set of permissions that define what actions are allowed on which resources.
- It is special set of permissions that you can assign to different services like EC2, S3 and many more.
- These permissions are attached to the role, not to an IAM User or a group.


# Multi-Factor Authentication-
- AWS multi-factor authentication (MFA) is an AWS Identity and Access Management (IAM) best practice that requires a second authentication factor in addition to user name and password sign-in credentials.
- You can enable MFA at the AWS account level for root and IAM users you have created in your account.
- It is a security feature that adds an extra layer of protection to user accounts by requiring multiple forms of verification before granting access.
  
