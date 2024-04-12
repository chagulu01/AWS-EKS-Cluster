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
