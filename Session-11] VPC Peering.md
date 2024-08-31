# VPC Peering-
- VPC peering is a networking connection between two VPC that allows them to communicate with each other as if they were part of the same network.
- It enables private connectivity between resources in different VPCs.
  
- **Transitive Peering-**
  - VPC peering does not support transitive routing, meaning you cannot route traffic through a peered VPC to reach another VPC.
  - To connect multiple VPCs, you need to establish direct peering connections between each pair of VPCs

# AWS Direct Connect-
- AWS Direct Connect makes it easy to establish a dedicated connection from an on-premises network to one or more VPCs.

# VPC Endpoint-
- A VPC Endpoint is a feature in AWS that allows private, secure access to AWS services and resources from within a VPC without the need for an internet gateway, NAT device or Direct Connect connection.

### Types of VPC Endpoints-
- **Interface Endpoints-**
  - Used for AWS PrivateLink to connect to AWS services privately through a network interface.
- **Gateway Endpoints-**
  - Gateway Endpoints are virtual devices that are used to connect to AWS services.
  - They add a route to your VPC route tables that points to the service.
 