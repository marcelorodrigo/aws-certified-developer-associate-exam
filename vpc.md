# Virtual Private Cloud
- VPC: private network (regional resource)
- Subnet: allows you to partition your VPC into smaller networks (availability zone resource)
- Public Subnet vs Private Subnet
- Route Tables: define acess to the internet and between subnets
- Internet Gateways: helps your VPC to reach internet (and being reachable)
- NAT Gateways: allow your instances in Private Subnets to access internet, but still remain private

## Network Access List
- Firewall which controls traffic from and to a subnet
- ALLOW and DENY rules available
- Subnet level
- Rules with only IP addresses

## Security Groups
- Firewall. which control traffic to and from an ENI/EC2 instances
- Only ALLOW rules available
- Rules with IP addresses and other security groups

## VPC Flow Logs
- Useful to analyze traffic to your VPC and auditing access
- Logs packets coming through subnets
- Aggregates packets according to a capture window

## VPC Peering
- Makes two VPC connect privately, as they were in the same network
- IP address range cannot be overlapping

## VPC Endpoints
- Allow you to connect AWS Services using a private network instead of public network
- Give you enhanced security and lower latency to AWS services
- Only used within your VPC
