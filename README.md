# Amazon F1 instance walk through tutorial

This tutorial uses the hello-world (RTL) design provided by aws-fpga but could be extended to other designs.
Additionally, the FPGA AMI version used is `1.3.4` and the git-tag of `aws-fpga` is `v1.3.6`.

1. [Create an AWS account](create_aws_account.md)
2. [Generate SSH keys](generate_ssh_keys.md)
3. [Create S3 credential](create_s3_credential.md)
4. [Increase instance limit](increase_instance_limit.md)
5. [Create an AMI instance](create_ami_instance.md)
6. [Configure S3 bucket](configure_s3.md)
7. [Setup development environment](setup_development_environment.md)
8. [Simulate the design](simulate_design.md)
9. Build the hardware design
10. [Generate the AFI](generate_afi.md)
11. [Program FPGA](program_fpga.md)
12. [Compile the runtime of the design](compile_runtime.md)
13. [Bookkeping the AFI](bookkeeping_afi.md)

After you finish this walk through tutorial, you will normally iterate step 8 and step 13
