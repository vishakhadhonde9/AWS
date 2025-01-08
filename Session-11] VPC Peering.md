# VPC Peering-
- VPC peering is a networking connection between two or more VPC that allows them to communicate with each other as if they were part of the same network.
- It enables private connectivity between resources in different VPCs.

![image](https://github.com/user-attachments/assets/f1cfccb9-f45e-4ab9-bebe-99a61d6bf308)

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
 
# Placement Group-
- When you launch a new EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures.
- To create a placement group, there are three placement strategies:
  - Cluster
  - Partition
  - Spread

## Cluster -
- A cluster placement group is a logical grouping of instances within a single Availability Zone.
- To achieve low-latency network performance and high-bandwidth connectivity between instances.
## Spread -
- A spread placement group is a logical grouping of instances that allows you to place instances on distinct hardware to reduce the risk of simultaneous failures that might occur when instances share the same equipment.
- To distribute instances across underlying hardware to reduce the risk of correlated failures.

## Partition-
- To distribute instances across multiple logical partitions within a single Availability Zone to minimize the risk of correlated hardware failures affecting all instances in the group.

# NIC-
- Network interface also known as an Elastic Network Interface is a virtual network interface that can be attached to an instance in a VPC.
- It provides a way for instances to connect to a network and communicate with other instances or external networks. 
