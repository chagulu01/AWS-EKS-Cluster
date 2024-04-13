Setup Kubernetes on Amazon EKS
You can follow the same procedure in the official AWS document Getting started with Amazon EKS – eksctl
Pre-requisites:  an EC2 Instance
Connecting to the instance: cd /c/Users/Biswajit.Sutar/.ssh/
AWS EKS Setup
Setup kubectl
a. Download kubectl version 1.20
b. Grant execution permissions to kubectl executable
c. Move kubectl onto /usr/local/bin
d. Test that your kubectl installation was successful

curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.19.6/2021-01-05/bin/linux/amd64/kubectl
chmod +x ./kubectl
mv ./kubectl /usr/local/bin 
kubectl version --short --client

> terraform-eks
A sample repository to create EKS on AWS using Terraform.

Install AWS CLI
As the first step, you need to install AWS CLI as we will use the AWS CLI (aws configure) command to connect Terraform with AWS in the next steps.

Follow the below link to Install AWS CLI.

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
Install Terraform
Next, Install Terraform using the below link.

https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli
Connect Terraform with AWS
Its very easy to connect Terraform with AWS. Run aws configure command and provide the AWS Security credentials as shown in the video.

Initialize Terraform
Clone the repository and Run terraform init. This will intialize the terraform environment for you and download the modules, providers and other configuration required.

Optionally review the terraform configuration
Run terraform plan to see the configuration it creates when executed.

Finally, Apply terraform configuation to create EKS cluster with VPC
terraform apply
