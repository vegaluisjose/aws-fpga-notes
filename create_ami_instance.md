# Create an AWS F1 instance

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
