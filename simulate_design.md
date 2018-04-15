# Simulate the design

1. [Change the instance type](change_instance_type.md) for a compute optimized instance (c4.4xlarge or c5.4xlarge)
1. Connect to the instance via ssh
1. Go to the **aws-fpga** folder `cd <the-path-of-aws-fpga-folder>`
1. Setup the hardware environment `source hdk_setup.sh`
1. Go to the hello-world example folder `cd hdk/cl/examples/cl_hello_world`
1. Export environment variable for the design `export CL_DIR=$PWD`
1. Go to the hello-world simulation scripts folder `cd hdk/cl/examples/cl_hello_world/verif/scripts`
1. make TEST=test_hello_world
