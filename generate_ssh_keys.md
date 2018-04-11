# Prepare ssh keys to access the [Amazon EC2 F1](https://aws.amazon.com/ec2/instance-types/f1/)

SSH keys are needed in order to connect to the instance. You could generate them locally in your computer or in the EC2 management console.

These steps were partially taken from [here](https://github.com/Xilinx/SDAccel_Examples/wiki/Prerequisites-for-working-with-SDAccel-on-AWS-F1).

1. Open the [EC2 Management Console](https://console.aws.amazon.com)
2. In the left pane, select **Key Pairs** from the **NETWORK & SECURITY** menu
3. Choose the **Create Key Pair** button
4. Name your key pair and choose **Create**. A .pem file will be automatically downloaded
5. Move the key file (.pem) to your `~/.ssh` folder
6. Change the permission of the key file (.pem) `chmod 400 <my-key-pair.pem>`
