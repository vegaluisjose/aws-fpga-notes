<table style="width:100%">
  <tr>
    <th width="100%"><h2>Table of contents (steps)</h2></th>
  </tr>
  <tr>
    <td><a href="create_aws_account.md">1. Create an AWS account</a></td>
  </tr>
  <tr>
    <td><a href="generate_ssh_keys.md">2. Generate SSH keys</a></td>
  </tr>
  <tr>
    <td><a href="create_s3_credential.md">3. Create S3 credential</a></td>
  </tr>
  <tr>
    <td><a href="request_access_f1.md">4. Request access to Amazon EC2 F1 instances</a></td>
  </tr>
  <tr>
    <td><a href="create_ami_instance.md">5. Create an AMI instance</a></td>
  </tr>
  <tr>
    <td><a href="configure_s3.md">6. Configure S3 bucket</a></td>
  </tr>
  <tr>
    <td><a href="setup_development_environment.md">7. Setup development environment</a></td>
  </tr>
  <tr>
    <td><a href="simulate_design.md">8. Simulate the design</a></td>
  </tr>
  <tr>
    <td><a href="build_hardware.md">9. Build the hardware design</a></td>
  </tr>
  <tr>
    <td><a href="generate_afi.md">10. Generate the AFI</a></td>
  </tr>
  <tr>
    <td><a href="program_fpga.md">11. Program the FPGA</a></td>
  </tr>
  <tr>
    <td><a href="compile_runtime.md">12. Compile the runtime of the design</a></td>
  </tr>
  <tr>
    <td><a href="bookkeeping_afi.md">13. Bookkeping the AFI</a></td>
  </tr>
</table>

---------------------------------------

# 3. Create [S3 buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingBucket.html) credentials

These buckets are require to generate the Amazon FPGA Image (AFI) from the generated design to program the FPGA.

Steps:

1. Open the [EC2 Management Console](https://console.aws.amazon.com)
2. Click on your **Name** on the top bar
3. Select **My Security Credentials**
4. Click **Users** from the left bar
5. Click **Add user** in blue
6. Create and add an username
7. Check the box **Programmatic access** on Access type
8. Click Next
9. Create a group name and assign a policy, the policy is **AmazonS3FullAccess** and **AmazonEC2FullAccess**
10. After creating the group, check the box for this new group
11. Click Next
12. Click **Create User**
13. Save the **AWS Access Key ID** and **AWS Secret Access Key**. You could also download this information in a (.csv) file.
Save this informaiton because it cannot retrieved in the future and you will have to create another user from scratch
