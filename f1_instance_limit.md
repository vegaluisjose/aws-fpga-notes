# Request access to Amazon EC2 F1 instances

By default, AWS users do not have access to F1 instances.
You need to request and be granted access to F1 instances before you can start using these instance.

These steps were partially taken from [here](https://github.com/Xilinx/SDAccel_Examples/wiki/Prerequisites-for-working-with-SDAccel-on-AWS-F1).

1. Open the Service Limit Increase [form](http://aws.amazon.com/contact-us/ec2-request)
2. Submit a **Service Limit Increase** for **EC2 Instances**
3. Select the region where you want to access F1 instances: US East (N.Virginia), US West (Oregon) or EU (Ireland)
4. Select the instance type, either **f1.2xlarge** or **f1.16xlarge**
5. Set the **New limit value** to **1** or more
6. Fill the rest of the form as appropriate and click **Submit**


**Requests are typically processed by AWS in 24 to 48 hours.**
