# Virtual Private Cloud(VPC)-
- AWS VPC allows you to launch resoureces inside isolated environment.
- You have complete control over your VPC, from creation to customization and even deletion.


# Architecture of VPC-

![image](https://github.com/user-attachments/assets/03416acb-6cbc-4c63-a2b9-b64f0e58be6b)

# Subnet-
- A subnet or subnetwork is a segment of a larger network designed to partition and manage traffic more efficiently.
- Subnets allow you to divide a VPC's IP address space into smaller, manageable segments. This segmentation helps in organizing resources and controlling traffic flow.
  ### Types of Subnet-

  **1] Public Subnet-**
    - Used for resources that need to be accessible from the internet.
    - These subnets have routes to an Internet Gateway (IGW), enabling outbound traffic to the internet and inbound traffic from the internet.

  **2] Private Subnet-**
    - Used for resources that do not need to be directly accessible from the internet.
    - These subnets do not have direct routes to an Internet Gateway. They can access the internet indirectly via a NAT Gateway or NAT Instance in a public subnet.
 

 # Internet Gateway-
 - An Internet Gateway is a horizontally scaled, redundant, and highly available component that allows communication between instances in your VPC and the internet.
 - To activate internet connectivity for your VPC, you must create an internet gateway.

# NAT(Network Address Translation) Gateway-
- NAT Gateway allows instances in a private subnet within a Virtual Private Cloud to initiate outbound traffic to the internet or other services while preventing inbound traffic from the internet.
- Instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.

# Security Group-








