### EC2 Intro
- Elastic Compute Cloud (Infrastructure as a Service)

### AMI
- Amazon Machine Image

### Copy this script

#!bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello world from $(hostname -f)</h1>" > /var/www/html/index.html

### Instance info
### Example: m5.2xlarge
- m: instance class
- 5: generation
- 2xlarge: size 

### Security Group
- firewall settings
- Inbound and outbound rules


### Access the EC2 instance via ssh
### Security group inbound rule: ssh protocol on port 22 open to all (0.0.0.0)
### Example: 3.68.105.86 is the public IP address fo the EC2 instance
### Note: we generate the ssh key when we are creating the EC2 instance
chmod 400 some-ssh-key.pem
ssh -i some-ssh-key.pem ec2-user@3.68.105.86

### check the ssh access is ok
whoami

### try to get list of users
### You first have to create a role with IAM read access and attach this role to the EC2 instance
aws iam list-users














