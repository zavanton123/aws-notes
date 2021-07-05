### AWS 
- Regions (us-east-1, eu-west-3...) are clusters of data centers
- Regions consist of Availability Zones (from 2 to 6). AZ is one (or more) data center.
- Points of Presence (Edge Locations)
- ARN (Amazon Resource Name)

### IAM Service
- Identity and Access Management
- This is a global service
- Root Account Vs Groups and Users
- Policies and Permissions
- Password Policy VS MFA (Multi Factor Authentication)

### How to access AWS?
- AWS Management Console
- AWS Command Line Interface (AWS CLI)
- AWS Software Development Kit (SDK)
 
### Access Key
- Access Key ID
- Secret Access Key

### How to install CLI?
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

### Check the CLI is installed successfully
aws --version

### Add the Access Key to the AWS CLI
aws configure

### Example: show all users
aws iam list-users

### AWS CloudShell

### Users VS Role
- Users are for regular users (i.e. people)
- Roles are for programmatic users (i.e.)

### AWS IAM Security Tools
- Credential Report
- Access Advisor





 