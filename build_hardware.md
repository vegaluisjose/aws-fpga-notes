# Build the hardware design

1. [Change the instance type](change_instance_type.md) for a compute optimized instance (c4.4xlarge or c5.4xlarge)
1. Connect to the instance via ssh
1. Go to the **aws-fpga** folder `cd <the-path-of-aws-fpga-folder>`
1. Setup the hardware environment `source hdk_setup.sh`
1. Go to the hello-world example folder `cd hdk/cl/examples/cl_hello_world`
1. Export environment variable for the design `export CL_DIR=$PWD`
1. Go to the hardware scripts folder `cd build/scripts`
1. Run `./aws_build_dcp_from_cl.sh`
1. Run `tail -f last_log` to monitor progress and exit anytime by running `ctrl+c`
1. Wait until Xilinx Vivado finishes building the design and the final design (.tar) will be located at `$CL_DIR/build/scripts/to_aws/*.Developer_CL.tar`
1. Copy the final tar-file to the s3 bucket `aws s3 cp $CL_DIR/build/checkpoints/to_aws/*.Developer_CL.tar s3://<your-s3-bucket>`
