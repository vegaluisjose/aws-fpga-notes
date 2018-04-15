# Configure s3 bucket

S3 bucket is needed for storing and generating the Amazon FPGA Image or AMI.

Steps:

1. Connect to your instance via ssh
1. Run `aws configure`
1. Answer the questions
```
AWS Access Key ID [None]: <your access key> 
AWS Secret Access Key [None]: <your secret key> 
Default region name [None]: <your AWS region, for instance us-west-2 for Oregon>
Default output format [None]: json
```
1. Create a s3 bucket for your design `aws s3 mb s3://<your-bucket-name>`
1. Test if the bucket was setup correctly:
    * Create a file `touch one-file.txt`
    * Copy file to s3 bucket `aws s3 cp one-file.txt s3://<your-bucket-name>`
    * List files in the s3 bucket `aws s3 ls s3://<your-bucket-name>`
    * Remove file `aws s3 rm s3://<your-bucket-name>/one-file.txt`
