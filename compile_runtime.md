# Compile the runtime of the design

1. Go to the **aws-fpga** folder `cd <the-path-of-aws-fpga-folder>`
1. Setup the software environment `source sdk_setup.sh`
1. Go to the hello-world example folder `cd hdk/cl/examples/cl_hello_world`
1. Export environment variable for the design `export CL_DIR=$PWD`
1. Go to the runtime folder `cd software/runtime`
1. Run `make all`
1. Run `sudo ./test_hello_world`
1. Look for `TEST PASSED` in the output of the program
1. This hello-world design uses a **virtual dip switch** that can be changed after programming the FPGA
    * The **virtual dip switch** can be changed by `sudo fpga-set-virtual-dip-switch -S 0 -D 1111111111111111`
