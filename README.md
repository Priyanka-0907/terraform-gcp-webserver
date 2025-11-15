# Terraform project to deploy a GCP VM, firewall rule, and Apache web server
Terraform GCP Web Server Deployment

This project demonstrates how to deploy a fully functional Apache Web Server on a Google Cloud Platform (GCP) Compute Engine VM using Terraform.
It includes automated provisioning of:

VPC Network
Firewall Rule (allowing HTTP traffic)
Compute Engine VM
Startup Script (installs Apache and hosts a custom webpage)

This project is suitable for DevOps, Cloud Engineer, and SRE portfolios.

# Architecture Overview

Terraform automatically creates the following resources on GCP:

1. VPC Network (default or custom)

2. Firewall Rule

      . Allows inbound traffic on port 80 (HTTP)

3. Compute Engine VM Instance

      . Region/Zone: us-west1 / us-west1-c

      . Machine type: e2-micro (lab-friendly)

4. Apache Web Server Deployment

      . Installed using a startup script

      . Hosts a sample webpage

      . Accessible via VM External IP


# Project Structure

├── main.tf            # VM, firewall, startup script
├── provider.tf        # Provider configuration
├── variables.tf       # Input variables
├── outputs.tf         # VM external IP output
├── README.md          # Project documentation


# Technologies Used

Terraform

Google Cloud Platform (GCP)

    . Compute Engine

    . VPC Networking

Apache Web Server

Startup Script Automation

 
# How to Deploy This Project
 
1️ Initialize Terraform
terraform init

2️ Preview the resources that will be created
terraform plan

3️ Deploy infrastructure
terraform apply


When prompted, type:
yes

# Accessing the Web Server

After the deployment is complete, Terraform outputs the VM’s External IP:

vm_external_ip = "34.xx.xx.xx"


Open this in a browser:

http://external_ip

You should see:

  "This VM was launched using Terraform!"

# Cleanup (Important for labs)

To avoid extra costs or to end the lab:

terraform destroy

Type yes when asked.


# Author

This project is part of my Cloud Engineer portfolio, showcasing real IAC deployment using Terraform and Google Cloud.
