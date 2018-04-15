# Generate the AFI

The Amazon FPGA Image or AFI is what it is used to program the FPGA or deploy the hardware

1. Make sure the final design (tar-file) and log file have been copied to the S3 bucket
1. Create a log file for monitoring AFI generation `touch log-file.log`
1. Copy log file to the s3 bucket `aws s3 cp log-file.log s3://<your-s3-bucket>`
1. Remove local log file `rm log-file.log`
1. Generate the AFI by running the following:

```
aws ec2 create-fpga-image --name <afi-name> \
                          --description <afi-description> \
                          --input-storage-location Bucket=<bucket-name>,Key=<path-to-tar-file> \
                          --logs-storage-location Bucket=<bucket-name>,Key=<path-to-log-file>
```
3. Copy and store the AFI and AGFI
4. Query if the AFI generation is done by `aws ec2 describe-fpga-images --fpga-image-ids <AFI ID>`
5. Wait until the AFI becomes available
```
{
    "FpgaImages": [
    {
        ...
        "State": {
            "Code": "available"
        },<
        ...
        "FpgaImageId": "afi-06d0ffc989feeea2a",
        ...
    }
    ]
}
```
