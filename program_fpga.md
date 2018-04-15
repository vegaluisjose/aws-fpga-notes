# Program Amazon F1 FPGA

1. Change to an FPGA instance **f1.2xlarge** or **f1.16xlarge**, [follow these steps](change_instance_type.md)
2. Connect the instance via ssh
3. Clear the FPGA `sudo fpga-clear-local-image -S 0`
4. Program the FPGA `sudo fpga-load-local-image -S 0 -I <FPGA-image-global-ID>`
5. Get info about the FPGA `sudo fpga-describe-local-image -S 0 -H`
6. The option **-S** is related to the ID of the FPGA, this is important for instances having more than
one FPGA i.e. **f1.16xlarge**
