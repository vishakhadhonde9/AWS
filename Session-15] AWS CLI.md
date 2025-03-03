# AWS CLI-
- Install AWS CLI (Command Line Interface):
- Configure AWS CLI Credentials:
    - aws configure
- Create EC2 Instance:
    - aws ec2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.micro --key-name MyKeyPair --security-groups MySecurityGroup

- Key-pair creation:
    - aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text> MyKeyPair.pem
    - chmod 400 MyKeyPair.pem
    - ssh -i MyKeyPair.pem ec2-user@<instance-public-ip>


- Create VPC:
    - aws ec2 create-vpc --cidr-block 10.0.0.0/16 --output json

- Create S3 Bucket -
    - aws s3api create-bucket --bucket <BUCKET_NAME> --region <REGION>

