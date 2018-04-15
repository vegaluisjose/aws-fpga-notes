# Program the FPGA

1. Change to an FPGA instance **f1.2xlarge** or **f1.16xlarge**, [follow these steps](change_instance_type.md)
1. Connect the instance via ssh
1. Clear the FPGA `sudo fpga-clear-local-image -S 0`
1. Program the FPGA `sudo fpga-load-local-image -S 0 -I <FPGA-image-global-ID>`
1. Get info about the FPGA `sudo fpga-describe-local-image -S 0 -H`
1. The option **-S** is related to the ID of the FPGA, this is important for instances having more than
one FPGA i.e. **f1.16xlarge**
