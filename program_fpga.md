# Program Amazon F1 FPGA

1. 


* Stop your c4.x4large instance
* Change instance type to f1
* Start instance f1
* Clear the FPGA sudo fpga-clear-local-image -S 0
* Program sudo fpga-load-local-image -S 0 -I <FpgaImageGlobalId>
* Get info sudo fpga-describe-local-image -S 0 -H
