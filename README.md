# WordPress_AWS
Hosted my wordpress website on AWS


#1. VPC Setup
Created 4 Subnets; 2 private subnets and 2 public subnets so that the components meant to be safeguarded can be stored in the private subnet and the components that should be publicly accessible stored in the public subnet


#2. NAT Gateway Architecture
Created a NAT Gateway so as to enable the private subnets to be able to interact with the interact via a internet gateway(IGW)


#3. AWS RDS MySQL Setup
Created a MySQL database to store the wordpress files, which can be easily retrieved using the MySQL workbench


#4. EFS Setup for Wordpress files
Created an EFS(Elastic File System) so as to store the Wordpress and make it scalable and shareable
Attached the EFS unto the Instance, so as to enable the instance interact with the files stored in the EFS


#5. Installation of Wordpress
Integrated Wordpress into the EC2 Instance, so as to make the Instance able to host the website publicly
#code used is kept in this repository#


#6. Application Load Balancer
Created a ALB with the EC2 instance as its target group(TG), so as to make sure loads are equally distributed amongst several/multiple instances/servers


#7. Auto Scaling Group
Created an ASG using the TG and and AMI(Image) using the EC2 instance, this image was used so as not to customize the ASG will be creating to look exactly as the instance it is imaging.
This ASG was created to enable the platform scale up or down according to the demand/traffic
