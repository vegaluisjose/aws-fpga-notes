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

# 5. Create an AWS F1 instance

These steps are partially taken from [here](https://github.com/Xilinx/SDAccel_Examples/wiki/Create,-configure-and-test-an-AWS-F1-instance)

1. Go to the [AWS EC2 dashboard](https://console.aws.amazon.com/ec2)
1. In the top right corner, select a region with F1 instances, such as **US West (Oregon)**
1. Click **Launch Instance**
1. Click **AWS Marketplace** (on the left pane, second item under Quick Start)
1. Search for **FPGA**
1. Select the **FPGA Developer AMI**
1. Click **Continue**
1. Select the instance type **c4.4xlarge** (developing) and **f1.2xlarge** (programming). This can be changed later on as well
1. Click **Next** until you reach the **Add storage** part and change that accordingly, default is 5GB for EBS Volume
1. These settings mentioned here are the minimum required for the FPGA instance, you could always configure other things
1. Go to the **Review** stage
1. Click **Launch**
1. Select the already generated ssh-keys or generate new ones in this stage
1. Return to [AWS EC2 dashboard](https://console.aws.amazon.com/ec2)
1. Click the **Instances**, in the left pane, to display the list of available instances
1. In the bottom pane, note the IPv4 Public DNS and Public IP address of the instance. You will need these to connect to your instance
1. You should be able to connect to the instance now:
    * Linux/Mac `ssh -i <your-key>.pem centos@<public-dns-ec2>`
    * Windows `putty -i <your-key>.ppk centos@<public-dns-ec2>`
