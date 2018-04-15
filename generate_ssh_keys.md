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

# 2. Prepare SSH keys to access the [Amazon EC2 F1](https://aws.amazon.com/ec2/instance-types/f1/)

SSH keys are needed in order to connect to the instance. You could generate them locally in your computer or in the EC2 management console.

These steps were partially taken from [here](https://github.com/Xilinx/SDAccel_Examples/wiki/Prerequisites-for-working-with-SDAccel-on-AWS-F1).

1. Open the [EC2 Management Console](https://console.aws.amazon.com)
1. In the left pane, select **Key Pairs** from the **NETWORK & SECURITY** menu
1. Choose the **Create Key Pair** button
1. Name your key pair and choose **Create**. A .pem file will be automatically downloaded
1. Move the key file (.pem) to your `~/.ssh` folder
1. Change the permission of the key file (.pem) `chmod 400 <my-key-pair.pem>`
