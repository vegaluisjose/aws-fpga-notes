# Simulate the design

1. [Change the instance type](change_instance_type.md) for a compute optimized instance (c4.4xlarge or c5.4xlarge)
2. Go to the **aws-fpga** folder `cd <the-path-of-aws-fpga-folder>`
3. Setup the hardware environment `source hdk_setup.sh`
4. Go to the hello-world simulation scripts folder `cd hdk/cl/examples/cl_hello_world/verif/scripts`
5. make TEST=test_hello_world
