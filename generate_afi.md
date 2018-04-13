# Generate the AFI

The Amazon FPGA Image or AFI is what it is used to program the FPGA or deploy the hardware

1. Make sure the final design (tar-file) and log file have been copied to the S3 bucket
2. Generate the AFI by running the following:

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
