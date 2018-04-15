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
    <td><a href="setup_development_environment..md">7. Setup development environment</a></td>
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

# 6. Configure s3 bucket

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
