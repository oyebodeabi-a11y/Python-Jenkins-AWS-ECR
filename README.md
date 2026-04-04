# Python-Jenkins-AWS-ECR
This is a project that builds a docker image of a python flask working application and pushing the Docker image built to AWS ECR (Elastic Container Registry) using Jenkins CICD pipeline. 

Tools:
# To install AWS CLI 
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
sudo apt-get install unzip -y
unzip awscliv2.zip
sudo ./aws/install

ECR is used to store or save Docker images with AWS cloud. I is safe, provate and much secure than Docker hub.

## To check AWS in installed
aws --version

# Additional Plugins in Jenkins:
AWS credentials

# AWS role
AWS role created - Admin access 

# AWS CLI 

##  Project tools used:

# 1. EC2, EC2 connect, security group jenkins port 8080
# 2. Jenkins software (for CICD process)
# 3. Python flask
# 4. AWS ECR

## Project Workflow:

# Step 1:

Launch a Jenkins server from EC2 instance:

1. Log into AWS console and launch an EC2 instance

2. Create a free tier ubuntu server

3. Add a security group  - Edit inbound rules for Jenkins on port 8080

4. Launch EC2 connect

# Step 2:

Update the system to install Jenkins with the prompts below:

5. sudo apt update -y

Install Jenkins

6. vi Jenkins.sh
7. Run Jenkins file (using code saved on vs code).

Ctrl c

8. Press Esc on keyboard, then type :wq!

9. Type chmod 777 Jenkins.sh

10.Type ./Jenkins.sh

To check is Jenkins is install on server:
11. Type sudo systemctl status Jenkins

12. Go back to the EC2 instance and copy the Public IP4 address

13. Paste in a browser and add :8080 press enter
14. In the Jenkins brower, copy the red link for admin password

15. Go to the EC2 browser, clear the terminal and type sudo cat right click and paste the red link

16. copy the password and paste in the Jenkins browser

# Step 3:

17. Once in Jenkins CICD:

18. Click on install suggested plug ins

19. Type username and password: bims Iwaro123

20. On Install config, click save and finish, start using Jenkins.

Once in the Jenkins env:
21. Click on the Manage Jenkins wheel

22. Click on Plugins, select Available Plugins

23. Search for AWS, select AWS credentials.

# Step 4:

24. Click on AWS EC2 connect, to run AWS CLI

#  AWS CLI allows the hand shake with AWS infrastructure.

25. Run script to install AWS CLI (script above).

# Step 5:

Create IAM User Role in AWS.

26. In EC2 env, type IAM in the search bar.

27. Create IAM user role

28. Go to ECR, Admin access, create role name, "Abi-role"

29. Go to EC2, click on the instance, action, add role, connect. 




