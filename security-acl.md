# Network Access Control List

- Filters traffic between subnets by IP address an port
- Thing about a ACL like a big security group that is acting over a subnet
- Subnets can share/use the same ACL
- **Network ACL rules have precedence over security groups rules**
- Network ACL rules applies only to inbound/egress traffic
- ACL rules are not applied for traffic inside the subnet (However, they work for traffic between subnets)
