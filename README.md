# Automated Web Server Deployment on Google Cloud Using Terraform

# Project Overview

This project demonstrates the automation of infrastructure deployment on Google Cloud Platform (GCP) using Terraform.
The setup includes provisioning a Compute Engine virtual machine, configuring firewall rules, installing Nginx automatically through a startup script, and validating deployment through a public web page.

This project reflects real-world cloud engineering skills such as infrastructure-as-code (IaC), VM provisioning, network configuration, and automation.


# Architecture Overview

Terraform automatically creates the following resources on GCP:

      VPC firewall rule allowing inbound HTTP (port 80)

      Compute Engine Virtual Machine (e2-micro)

      Startup script that auto-installs Nginx

      Publicly accessible web server with a custom message

     

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

    . Firewall

Nginx

Startup Script Automation

 
# How to Deploy This Project
 
1️ Initialize Terraform
      
      terraform init

2️ Preview the resources that will be created
      
      terraform plan

3️ Apply and provision the infrastructure

      terraform apply

When prompted for variables (such as project_id), enter the values from your GCP environment.

Terraform will create:

      Firewall rule

      VM instance

      Automatic installation of Nginx
      

# Verify Deployment

a. From Google Cloud Console

Navigate to:
Google Cloud Console → Compute Engine → VM Instances
Confirm the VM named portfolio-vm is running.

b. Test the web server

Copy the VM's External IP from the console.
Paste it into browser:
      http://external-ip

You should see the custom webpage deployed by the startup script.


# Cleanup (Destroy Resources)

Run the command below to delete all provisioned GCP resources:

      terraform destroy

This is a best practice to avoid unnecessary cloud charges and maintain a clean project.


# Author

This project is part of my Cloud Engineer portfolio, showcasing real IAC deployment using Terraform and Google Cloud.
