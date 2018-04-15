# Program Amazon F1 FPGA

1. Go to the [AWS EC2 dashboard](https://console.aws.amazon.com/ec2)
2. Click the **Instances**, in the left pane
3. In case the current **Instance Type** is not an FPGA instance **f1.2xlarge** or **f1.16xlarge**:
    * Right click on the **Instance**, select **Instance State**, and select **Stop**
    * Wait until the instance is stopped
    * Right click on the **Instance**, select **Instance Settings**, and select **Change Instance Type**
    * Select from the drop-down menu an FPGA instance **f1.2xlarge** or **f1.16xlarge**
    * Right click on the **Instance**, select **Instance State**, and select **Start**
4. Every time an instance is stopped and launched again, AWS assigns a new IP to that instance
5. Copy the IP from the [AWS EC2 dashboard](https://console.aws.amazon.com/ec2)
6. Connect the instance via ssh
7. Clear the FPGA `sudo fpga-clear-local-image -S 0`
8. Program the FPGA `sudo fpga-load-local-image -S 0 -I <FPGA-image-global-ID>`
9. Get info about the FPGA `sudo fpga-describe-local-image -S 0 -H`
10. The option **-S** is related to the ID of the FPGA, this is important for instances having more than
one FPGA i.e. **f1.16xlarge**
