# Finance-Network-Security
Securing a financial network using Azure security technologies. 
Project: Secure Transactions Over Network Using Azure Security Technologies
Project Demo Link: https://jem68.github.io/Finance-Network-Security/
Project Overview
This project will cover the following key components:

Azure Virtual Network (VNet): Setting up a virtual network to host resources.
Azure Virtual Machine (VM): Creating VMs to host application components.
Network Security Groups (NSGs): Configuring security rules for network traffic.
Azure Firewall: Centralizing network security policies.
Azure Key Vault: Managing secrets and certificates.
Azure Application Gateway with WAF: Providing application delivery controller with Web Application Firewall.
Azure SQL Database: Hosting the database securely.
Azure Bastion: Secure and seamless RDP and SSH connectivity to your VMs.
Azure Monitor and Azure Security Center: Monitoring and managing security posture.
Azure DevOps: Integrating GitHub for CI/CD pipelines.
Step-by-Step Guide
1. Set Up Azure Virtual Network (VNet)
Create a VNet:
Go to the Azure portal.
Navigate to "Create a resource" and select "Virtual Network".
Configure the VNet with appropriate address space (e.g., 10.0.0.0/16).
Create subnets within the VNet (e.g., frontend subnet: 10.0.1.0/24, backend subnet: 10.0.2.0/24, and DMZ subnet: 10.0.3.0/24).
2. Create Virtual Machines (VMs)
Create VMs for Application Components:

Navigate to "Create a resource" and select "Virtual Machine".
Configure VM details (e.g., Ubuntu Server, Standard B2ms).
Place frontend VMs in the frontend subnet, backend VMs in the backend subnet, and security components in the DMZ subnet.
Install Required Software on VMs:

SSH into the VMs.
Install necessary software (e.g., web server, application server, etc.).
3. Configure Network Security Groups (NSGs)
Create NSGs:

Go to "Create a resource" and select "Network Security Group".
Add inbound and outbound security rules to control traffic flow between subnets and from the internet.
Associate NSGs with Subnets/VMs:

Navigate to the subnet or network interface of the VMs.
Associate the NSG with the subnet/VM.
4. Implement Azure Firewall
Create Azure Firewall:

Go to "Create a resource" and select "Firewall".
Configure the firewall to centralize network security policies.
Configure Firewall Rules:

Define rules to control traffic flow between different subnets and to/from the internet.
5. Set Up Azure Key Vault
Create Azure Key Vault:

Go to "Create a resource" and select "Key Vault".
Store sensitive information such as database connection strings, API keys, and certificates.
Access Key Vault in Application:

Configure the application to access secrets from Azure Key Vault using Managed Identity.
6. Set Up Azure Application Gateway with WAF
Create Application Gateway:

Go to "Create a resource" and select "Application Gateway".
Configure the application gateway with frontend IP, backend pool, and routing rules.
Enable Web Application Firewall (WAF) for additional security.
Add SSL Termination:

Upload SSL certificates to Azure Key Vault.
Configure the application gateway to use SSL certificates.
7. Configure Azure SQL Database
Create Azure SQL Database:

Go to "Create a resource" and select "SQL Database".
Configure the database with firewall rules to restrict access.
Secure Database Access:

Use Azure Key Vault to manage database credentials.
Configure the database to allow connections only from specific VNet subnets.
8. Implement Azure Bastion
Create Azure Bastion:
Go to "Create a resource" and select "Bastion".
Configure Bastion to securely connect to your VMs without exposing RDP/SSH ports.
9. Set Up Azure Monitor and Azure Security Center
Enable Azure Monitor:

Go to "Create a resource" and select "Monitor".
Configure monitoring for VMs, application gateway, and other resources.
Enable Azure Security Center:

Go to "Security Center" and enable it.
Configure security policies and enable recommendations.
10. Set Up CI/CD with GitHub and Azure DevOps
Create a GitHub Repository:

Initialize a GitHub repository to store the fintech application code.
Set Up Azure DevOps Project:

Navigate to Azure DevOps and create a new project.
Link the GitHub repository to Azure DevOps.
Create CI/CD Pipelines:

In Azure DevOps, set up build pipelines to automate the build process.
Configure release pipelines to deploy the application to Azure VMs.
