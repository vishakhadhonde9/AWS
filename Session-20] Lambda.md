# Amazon Lambda-
- You can use AWS Lambda to run code without provisioning or managing servers.
- Save costs by paying only for the compute time you use.
- 
### Lambdas Functions?
- AWS lambda are server-less compute functions are fully managed by the AWS where developers can run there code without worrying about servers.
- AWS lambda functions will allow you to run the code with out provisioning or managing servers.
- AWS lambda function will support different programming languages. You can build the function with the language at your convenience. Following are some languages supported by AWS lambda:
  - Python.
  - Node.js.
  - Java.
  - C#.
  - PowerShell.
  - Go.

 ![image](https://github.com/user-attachments/assets/609f32f7-e426-4214-a723-0b150b23c5dd)





# Code for lambda Function-
import json
import boto3
import urllib

def lambda_handler(event, context):
    s3_client = boto3.client('s3')  
    bucket_name = event['Records'][0]['s3']['bucket']['name']
    key = urllib.parse.unquote_plus(event['Records'][0]['s3']['object']['key']

    message = 'File ' + key + ' is successfully uploaded in bucket ' + bucket_name
    print(message)
    
    response = s3_client.get_object(Bucket=bucket_name, Key=key)
    contents = response["Body"].read().decode('utf-8')  # Specify the encoding
    contents = json.loads(contents)
    print("The data in the file is : \n", contents)
	




