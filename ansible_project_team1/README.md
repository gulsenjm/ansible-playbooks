Create the VPC using ansible. Make sure the code work in every region of AWS. 
VPC

6 subnets

   3 private 

   3 public 

Public subnets should have IGW attached to it. 

Private subnets should have NG attached to it. 

Configure route tables properly. Once private and public subnet created, please create ec2 instance (manually) on public subnet and ping google.com. If everything is successful, you should have proper response

Requirements
In order to work with Python 2.7.16, install next packages:

yum install ansible -y

amazon-linux-extras install ansible2

yum install python-boto3 -y

yum install python-pip -y

pip install boto awscli
