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

# 4. Request access to Amazon EC2 F1 instances

By default, AWS users do not have access to F1 instances.
You need to request and be granted access to F1 instances before you can start using these instance.

These steps were partially taken from [here](https://github.com/Xilinx/SDAccel_Examples/wiki/Prerequisites-for-working-with-SDAccel-on-AWS-F1).

1. Open the Service Limit Increase [form](http://aws.amazon.com/contact-us/ec2-request)
1. Submit a **Service Limit Increase** for **EC2 Instances**
1. Select the region where you want to access F1 instances: US East (N.Virginia), US West (Oregon) or EU (Ireland)
1. Select the instance type, either **f1.2xlarge** or **f1.16xlarge**
1. Set the **New limit value** to **1** or more
1. Fill the rest of the form as appropriate and click **Submit**


**Requests are typically processed by AWS in 24 to 48 hours.**
