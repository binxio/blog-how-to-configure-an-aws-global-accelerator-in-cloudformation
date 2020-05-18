# AWS Global Accelerator in CloudFormation

code for [blog Global Accelerator in CloudFormation](https://binx.io/blog/2019/07/10/how-to-configure-an-aws-global-accelerator-in-cloudformation/)

### Deploy the demo
In order to deploy the demo, type:

```sh
git clone https://github.com/binxio/blog-how-to-configure-an-aws-global-accelerator-in-cloudformation.git
cd blog-how-to-configure-an-aws-global-accelerator-in-cloudformation
pip install sceptre
sceptre launch -y demo
```

to view the application, type:`

```sh
DNS_NAME=$(
  aws --region us-west-2 globalaccelerator \
  list-accelerators \
    --output text \
    --query 'Accelerators[?Name==`cfn-global-accelerator-demo-us-west-2-accelerator`].DnsName')

open http://$DNS_NAME
```
