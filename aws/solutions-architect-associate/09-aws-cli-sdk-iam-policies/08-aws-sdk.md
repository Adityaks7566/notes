# AWS SDK Overview

- What if you want to perform actions on AWS directly from your applications code? (Without using the CLI).
- You can use SDK (Software development kit)
- Official SDKs are:
    - Java
    - .NET
    - Node.js
    - PHP
    - Python (named boto3 / botocore)
    - Go
    - Ruby
    - C++
- We have to use the AWS SDK when coding against AWS Services such as DynamoDB
- The AWS CLI uses the Python SDK (boto3)
- Good to know: if you don't specify or confiugure a default region, then us-east-1 will be chosed by default.

- It's recommended to use the default credential provider chain
- The default credential provider chain works seamlessly with:
    - AWS credentials at `~/.aws/credentials/` (only on our computers or on premise)
    - Instance Profile Credentials using IAM Roles (fro EC2 machines, etc)
    - Environment variables (AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY)
- Overall, never store aws credentials in your code.
- Best practice is for credetnials to be inherited from mechanisms above and 100% IAM Roles if working from within AWS services.