**Jenkins Installation on AWS EC2 with Terraform**
This Terraform project deploys Jenkins on an AWS EC2 instance. It includes configurations for setting up the necessary security group, EC2 instance, and an S3 bucket for Jenkins artifacts.

Prerequisites
Before you begin, ensure you have:

Terraform installed: terraform --version
AWS credentials configured (either via environment variables or AWS CLI): aws sts get-caller-identity
Usage
Clone this repository:
git clone <repository_url>, git clone https://github.com/VishAstra/Jenkins-aws-setup-with-terrafom.git


2. Navigate to the project directory:

cd terraform-jenkins-installation


3. Initialize Terraform:

terraform init


4. Review and customize the variables in `variables.tf` as needed.

5. Deploy the infrastructure:

terraform apply

Jenkins will be accessible via the public IP of the EC2 instance. Retrieve the IP from the Terraform outputs:
terraform output ec2_instance_public_ip


7. Access Jenkins by opening a web browser and navigating to:

http://<EC2_Instance_IP>:8080


8. Follow the on-screen instructions to complete the Jenkins setup.

## Variables

* `region` (required): The AWS region where the resources will be created.
* `security_group_name` (required): The name of the security group.
* `vpc_id` (required): The ID of the VPC where the resources will be deployed.
* `instance_ami` (required): The AMI ID for the EC2 instance.
* `instance_type` (required): The EC2 instance type.








