# Compile the runtime of the design

1. Go to the **aws-fpga** repository `cd aws-fpga`
2. Setup the environment `source sdk_setup.sh`
3. Go to the hello-world example folder `cd hdk/cl/examples/cl_hello_world`
4. Export environment variable for the design `export CL_DIR=$PWD`
5. Go to the runtime folder `cd software/runtime`
6. Run `make all`
7. Run `sudo ./test_hello_world`
8. Look for `TEST PASSED` in the output of the program
9. This hello-world design uses a **virtual dip switch** that can be changed after programming the FPGA
    * The **virtual dip switch** can be changed by `sudo fpga-set-virtual-dip-switch -S 0 -D 1111111111111111`
