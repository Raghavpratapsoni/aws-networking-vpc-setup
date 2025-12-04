# aws-networking-vpc-setup
This project focuses on building a basic network setup inside AWS using a custom VPC. The goal was to create a secure and organized network environment that supports both public-facing and private resources. The VPC was designed with two public subnets and two private subnets.

One main VPC acting as the private network boundary.

Two Public Subnets placed across different Availability Zones to improve reliability. These subnets allow resources to get public IPs and talk to the internet.

Two Private Subnets also spread across AZs, meant for backend services or databases that shouldn't be exposed publicly.

An Internet Gateway (IGW) attached to the VPC so public subnets can reach the internet.

A NAT Gateway, placed inside a public subnet, allowing private subnet resources to download packages or updates without exposing them directly.

Separate Route Tables for public and private paths to maintain clean network separation.

CIDR RANGES USED:
VPC: 10.10.0.0/16

Public Subnet A: 10.10.0.0/20  
Public Subnet B: 10.10.16.0/20  

Private Subnet A: 10.10.32.0/20  
Private Subnet B: 10.10.48.0/20  
