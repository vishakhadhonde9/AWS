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

# Route Tables-
- A route table contains a set of rules, called routes, that determine where network traffic is directed.
- When you create a VPC, AWS creates a route table called the main route table.
- You cannot delete the main route table.

# Security Group-
- It is act as firewall that control traffic to instance.
- It helps protect your server by specifying which types of network traffic are allowed to reach it.
#### Rules for Traffic:
    - Inbound Rules: Define what kind of incoming traffic (data coming into your server) is allowed. 
    - Outbound Rules: Define what kind of outgoing traffic (data going from your server) is allowed.
    
# Network Access Control List (NACL)-
- Network Access Control List (NACL) is used to control inbound and outbound traffic at the subnet level within a Virtual Private Cloud (VPC).
- It provides an additional layer of security by setting rules that determine which traffic is allowed or denied to and from resources within a subnet.
- It is act as firewall at subnet level.

# VPC Limits

| Component                     | Default Limit |
|-------------------------------|---------------|
| VPC                           | 5 per Region  |
| Subnets                       | 200 per VPC   |
| Route Tables                  | 200 per VPC   |
| Internet Gateway              | 5 per VPC     |
| NAT Gateway                   | 5 per AZ      |
| Virtual Private Gateway       | 5 per Region  |
| Customer Gateway              | 50 per Region |
| VPC Peering Connection        | 50 per VPC    |
| Security Groups               | 2,500 per VPC |
| Network ACLs                  | 200 per VPC   |
| Elastic IP Addresses          | 5 per Region  |
| DHCP Option Sets              | 10 per Region |
| Egress-Only Internet Gateway  | 5 per VPC     |
| Transit Gateway               | 5 per Region  |

# Diffrenece Between Security Group and NACl-
| **Aspect**                   | **Security Groups**                                                                             | **Network Access Control Lists (NACLs)**                                                            |
|------------------------------|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **Rules Supported**          | Supports only **allow** rules. By default, all traffic is denied unless explicitly allowed. Cannot deny specific traffic. | Supports both **allow** and **deny** rules. By default, all traffic is denied unless explicitly allowed or denied. |
| **Statefulness**             | **Stateful:** Inbound rules automatically reflect in outbound traffic. For example, if you allow inbound traffic on port 80, outbound responses are allowed automatically. | **Stateless:** Inbound and outbound rules are independent. Changes in inbound rules do not affect outbound rules. For example, if you add an inbound rule for port 80, you must separately add an outbound rule for port 80. |
| **Association**              | Associated with **EC2 instances**                       | Associated with **subnets** within a VPC.                                                           |
| **Rule Evaluation**          | All rules are evaluated before deciding whether to allow traffic.                              | Rules are evaluated in order, starting from the lowest number. The first matching rule determines the action. |
| **Application**              | Applied to an instance **at launch** or by modifying instance attributes.                      | Automatically applied to all instances **within the subnet**.                                        |






