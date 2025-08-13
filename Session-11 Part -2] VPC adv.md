# Bastion Host -
-  Bastion Host is a secure entry point to your private network or private subnet in the cloud.
-  Acts as Jump Server, for accessing private instances located within an AWS VPC.
-  Its primary purpose is to provide a controlled and secure point of entry into a private network from an external network, such as the internet.
-  From the Bastion Host, you connect to private EC2 instances that do not have public IP addresses.
-  This avoids exposing your private resources directly to the internet.

## Implementation -

- Create VPC (10.0.0.0/16)

- Create Subnets

   - Public Subnet: 10.0.1.0/24
   - Private Subnet: 10.0.2.0/24

- Create and Attach Internet Gateway to VPC

- Create Route Tables

   - PublicRT → route 0.0.0.0/0 to IGW, associate with Public Subnet
   - PrivateRT → associate with Private Subnet

- Create Security Groups

      BastionSG: SSH (22) from My IP
      PrivateSG: SSH (22) from BastionSG only

- Launch Bastion Host in Public Subnet with Public IP, attach BastionSG
- Launch Private EC2 in Private Subnet without Public IP, attach PrivateSG

- SSH Connection
- Bastion →

          ssh -i bastion-key.pem ec2-user@<BastionPublicIP>

- Private EC2 →
  
            ssh ec2-user@<PrivateIP>
            ssh -i <path_to_private_instance_key_on_bastion_host> ec2-user@<Private_Instance_Private_IP>

  - Note: If your private instances use a different key pair than the bastion host, you will need to copy the private key for the private instances to the bastion host.
