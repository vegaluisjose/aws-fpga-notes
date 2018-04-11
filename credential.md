# Create [S3 buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingBucket.html) credentials

These buckets are require to generate the Amazon FPGA Image (AFI) from the generated design to program the FPGA.

Steps:

1. Open the [EC2 Management Console](https://console.aws.amazon.com)
2. Click on your **Name** on the top bar
3. Select **My Security Credentials"
4. Click **Users** from the left bar
5. Click **Add user** in blue
6. Create and add an username
7. Check the box **Programmatic access** on Access type
8. Click Next
9. Create a group name and assign a policy, the policy is **AmazonS3FullAccess**
10. After creating the group, check the box for this new group
11. Click Next
12. Click **Create User**
13. Save the **AWS Access Key ID** and **AWS Secret Access Key**. You could also download this information in a (.csv) file.
Save this informaiton because it cannot retrieved in the future and you will have to create another user from scratch
