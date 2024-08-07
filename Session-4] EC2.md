# Instance Pricing-
## 1] On-demand pricing -
- You have to pay for compute capacity by the hour or second depending on which instance that you run.
- There is no longter commitments or upfront payments required.
- Charged based on the instance type, region, and usage time.

  
## 2] Reserved Instance-
- Purchase capacity for a one-year or three-year term with a significant discount compared to On-Demand pricing.
- You can save up to 75% discount compared to On-Demand.
- Payment Options:
     - All Upfront: Pay the entire cost upfront for the term.
     - Partial Upfront: Pay part of the cost upfront and the rest in monthly payments.
     - No Upfront: Pay when over the term.
       
## 3] Saving Plan-
- Flexible pricing model that offers savings over On-Demand pricing in exchange for a commitment to a consistent amount of usage (measured in $/hour) for a one-year or three-year term.
- Similar to Reserved Instances for pricing, with options for All Upfront, Partial Upfront, or No Upfront payments.
- Flexible across instance types and regions, without capacity reservation.


## 4] Spot Instance-
- Purchase unused EC2 capacity at a discount compared to On-Demand pricing.
- Spot Instances can be interrupted by AWS with little notice if AWS needs the capacity back.
- Used for application that have flexible start and end times.
- You can save upto 90% compared to on-demand price.
- You can set limit on how much you want to pay per hour.

## 5] Dedicated Hosts-
- A Dedicated Host is a physical EC2 server dedicated for your use.
- It provide isolation
- Dedicated Hosts can help you reduce costs by allowing you to use your existing server, software licenses like Windows server, SQL server etc.
- Customers who choose Dedicated Hosts have to pay the On-Demand price for every hour the host is active in the account


# Remote Access To Machines-

- **What is RDP?**
     - The Remote Desktop Protocol is solely used for accessing Windows virtual machines (VMs) and physical Windows servers.
     - Port: Default port is 3389.
     - From a user perspective, RDP provides a Windows Graphical User Interface (GUI) experience, making servers more accessible to a wider range of employees  with or without a technical background.
 
- **What is SSH?**
    - Secure Shell is a protocol optimized for Linux server access, but usable across any operating system’s server.
    - Port: Default port is 22.
    - Unlike RDP, SSH has no GUI, only command line interfacing, which is generally controlled through bash. As such, SSH is technically demanding for end users, and even more technically demanding to set up.
    







