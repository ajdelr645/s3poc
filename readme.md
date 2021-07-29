#this project contains cloudformation script for the S3 POC setup. 
#in this setup, you can use any on-premise projects to upload files 
#to the s3 bucket programmatically


## Usage

```
1. Upload lambdasns.zip into the codebucket 
2. First launch the Secondary CRR bucket template in secondary region. File is named accordingly based on order to launch. Note the KMS key arn from this stack
3. Launch the primary bucket template and input all the parameters. Use the KMS key arn obtained form the above stack for 's3CRRKmsKeyArn'
and for 'ReplicationBucketName' input the same CRR bucket name you gave in first stack without the Environment variable.
```