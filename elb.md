# Elastic Load Balancing

- ELB are servers that forward traffic from internet to multiple EC2 instances
- Provides SSL termination
- Enforces session stickness (cookie)
- High Availability through multiple availability zones (AZ)
- Separates public traffic from internal traffic
- Health Checks
  - ELB performs regular helth checks on allocated instances
  - If one instance does not provide 200 (OK), is marked as unhealthy
