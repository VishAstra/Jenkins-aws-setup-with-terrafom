Thank you for providing the `script.sh` file. This script seems to be for setting up Jenkins on an EC2 instance. 

Let's proceed to create a `README.md` file for your project. Here's a basic template for your README file:

```markdown
# Jenkins Installation on AWS EC2 with Terraform

This Terraform project deploys Jenkins on an AWS EC2 instance. It includes configurations for setting up the necessary security group, EC2 instance, and an S3 bucket for Jenkins artifacts.

## Prerequisites

Before you begin, ensure you have:

- [Terraform](https://www.terraform.io/downloads.html) installed.
- AWS credentials configured (either via environment variables or AWS CLI).

## Usage

1. Clone this repository:

   ```bash
   git clone <repository_url>
   ```

2. Navigate to the project directory:

   ```bash
   cd terraform-jenkins-installation
   ```

3. Initialize Terraform:

   ```bash
   terraform init
   ```

4. Review and customize the variables in `variables.tf` as needed.

5. Deploy the infrastructure:

   ```bash
   terraform apply
   ```

6. Jenkins will be accessible via the public IP of the EC2 instance. Retrieve the IP from the Terraform outputs.

7. Access Jenkins by opening a web browser and navigating to:

   ```text
   http://<EC2_Instance_IP>:8080
   ```

8. Follow the on-screen instructions to complete the Jenkins setup.

## Variables

- `region`: The AWS region where the resources will be created.
- `security_group_name`: The name of the security group.
- `vpc_id`: The ID of the VPC where the resources will be deployed.
- `instance_ami`: The AMI ID for the EC2 instance.
- `instance_type`: The EC2 instance type.

