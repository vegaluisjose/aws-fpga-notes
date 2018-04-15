<table style="width:100%">
  <tr>
    <th width="100%" colspan="5"><h2>Table of contents (steps)</h2></th>
  </tr>
  <tr>
    <td width="10%" align="center"><a href="create_aws_account.md">1</a></td>
    <td width="10%" align="center"><a href="generate_ssh_keys.md">2</a></td>
    <td width="10%" align="center"><a href="create_s3_credential.md">3</a></td>	  
    <td width="10%" align="center"><a href="increase_instance_limit.md">4</a></td>
    <td width="10%" align="center"><a href="create_ami_instance.md">5</a></td>
    <td width="10%" align="center"><a href="configure_s3.md">6</a></td>	  	  
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
