# Bookkeeping the AFI

Once you are done with the FPGA AFI, you can delete the image by:
```
aws ec2 --region us-west-2 delete-fpga-image --fpga-image-id <FPGA-image-ID>`

```
The image-ID used in this command is not global, since the region is specified (us-west-2).
