# Assignment-2.12

Given a Lambda function that is triggered upon the creation of files in an S3 bucket, answer the following: 

1. What is the purpose of the execution role on the Lambda function?

The execution role (IAM role) assigned to the Lambda function defines the permissions the function has to interact with AWS services and resources. When the function runs, it assumes this role, and any actions it performs (i.e. accessing S3.) are governed by the permissions in this role.

2. What is the purpose of the resource-based policy on the Lambda function? 

The resource-based policy on the Lambda function specifies who or what can invoke the function. This policy is attached to the Lambda function itself and grants permission to other AWS services, AWS accounts, or principals (in the case S3) to trigger the function.

3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies) - What is the needed update on the execution role? - What is the new resource-based policy that needs to be added (if any)? 

The execution role must be updated to include permissions for the Lambda function to upload files into the target S3 bucket
Action: s3:PutObject

