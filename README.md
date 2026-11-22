# azure-network-security-lab
Azure hands-on networking lab using Virtual Networks, subnets, NSGs, IP addressing, and security rules. Copy description
# Azure Network Security Lab

## Project Overview
This project demonstrates hands-on cloud networking configuration using Microsoft Azure. I built a virtual network, configured subnet IP addressing, created a Network Security Group (NSG), associated the NSG with a subnet, and reviewed inbound and outbound security rules.

The goal of this lab was to understand how Azure networking works and how network security controls help manage and protect cloud resources.

## Project Objectives
- Create and understand Azure Resource Groups
- Build a Virtual Network (VNet)
- Configure subnet address ranges
- Understand IPv4 and CIDR notation
- Create a Network Security Group (NSG)
- Associate an NSG with a subnet
- Review inbound and outbound security rules
- Understand Azure default security rules
- Practice cloud networking without deploying paid compute resources

## Technologies & Environment
- Cloud Platform: Microsoft Azure
- Networking: Azure Virtual Network (VNet)
- Network Segmentation: Subnets
- Security: Network Security Groups (NSG)
- IP Addressing: IPv4, CIDR
- Operating Environment: Windows PC, Azure Portal
- Documentation: Markdown
- Portfolio Platform: GitHub

## Lab Architecture

Virtual Network: 10.0.0.0/16
└── Subnet: default — 10.0.0.0/24
    └── Network Security Group: NSG-Compute-Lab

## Configuration Details

### Virtual Network
- Name: VNet-Compute-Network-Lab
- Region: East US 2
- Address Space: 10.0.0.0/16
- DNS: Azure-provided DNS

### Subnet
- Name: default
- Address Range: 10.0.0.0/24

### Network Security Group
- Name: NSG-Compute-Lab
- Region: East US 2
- Associated with: default subnet

## Inbound Security Rules

I reviewed the default inbound rules in Azure:

| Priority | Rule | Action |
|---|---|---|
| 65000 | AllowVnetInBound | Allow |
| 65001 | AllowAzureLoadBalancerInBound | Allow |
| 65500 | DenyAllInBound | Deny |

These rules control incoming network traffic based on source, destination, protocol, port, and priority.

## Outbound Security Rules

I reviewed the default outbound rules:

| Priority | Rule | Action |
|---|---|---|
| 65000 | AllowVnetOutBound | Allow |
| 65001 | AllowInternetOutBound | Allow |
| 65500 | DenyAllOutBound | Deny |

These rules control traffic leaving network resources.

## Project Steps

1. Created an Azure Resource Group.
2. Created a Virtual Network.
3. Defined the VNet address space.
4. Created and reviewed the subnet.
5. Created a Network Security Group.
6. Associated the NSG with the subnet.
7. Reviewed default inbound security rules.
8. Reviewed default outbound security rules.
9. Reviewed the VNet address space and CIDR configuration.
10. Verified the subnet association.

## Security Concepts Learned

- Network isolation using Virtual Networks
- Subnetting and IP address management
- CIDR notation
- Inbound versus outbound traffic
- Network Security Group filtering
- Rule priority and traffic evaluation
- Default Azure network security rules

## Cost Management

To avoid unnecessary costs, I did not deploy a virtual machine. This lab focused on Azure networking configuration and security concepts without deploying paid compute resources.

## What I Learned

This project gave me practical experience navigating the Azure Portal, creating cloud networking resources, configuring network security, understanding IP address ranges, and reviewing traffic rules.

It helped me develop foundational cloud infrastructure and troubleshooting skills relevant to entry-level IT support, cloud support, and cloud administration roles.

## Screenshots & Evidence

Screenshots documenting the configuration and steps performed will be added to this repository.

## Author

Hands-on Azure Cloud Networking Project

## Environment and Technologies

- Cloud Platform: Microsoft Azure
- Environment: Azure Portal (Web Browser)
- Virtual Networking: Azure Virtual Network (VNet)
- Subnet: Default subnet (10.0.0.0/24)
- Network Security: Network Security Group (NSG)
- IP Addressing: IPv4, CIDR notation
- Region: East US 2
- Operating System: Windows 11
- Documentation: GitHub Markdown

## Network Architecture

The project uses an Azure Virtual Network with the address space 10.0.0.0/16.

A subnet named default was created with the address range 10.0.0.0/24.

A Network Security Group (NSG) named NSG-Compute-Lab was created and associated with the subnet to control network traffic.

No virtual machine was deployed because I wanted to avoid incurring cloud compute charges during this lab.

## Security Configuration

- Created a Network Security Group.
- Associated the NSG with the virtual network subnet.
- Reviewed inbound security rules.
- Reviewed outbound security rules.
- Examined Azure default rules.
- Learned how Azure evaluates traffic based on rule priorities.
- Avoided deploying paid compute resources.

## Cost Management

This lab was designed to minimize costs. No virtual machines, public IP addresses, NAT gateways, or other chargeable compute resources were intentionally deployed.

## Skills Demonstrated

- Azure resource management
- Virtual network configuration
- Subnet planning
- IPv4 and CIDR addressing
- Network security groups
- Inbound and outbound traffic rules
- Cloud security fundamentals
- Cost-conscious cloud deployment
- Technical documentation
