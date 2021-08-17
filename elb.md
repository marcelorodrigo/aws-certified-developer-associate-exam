# Elastic Load Balancing

- ELB are servers that forward traffic from internet to multiple EC2 instances
- Provides SSL termination
- Enforces session stickness (cookie)
- High Availability through multiple availability zones (AZ)
- Separates public traffic from internal traffic
- Health Checks
  - ELB performs regular helth checks on allocated instances
  - If one instance does not provide 200 (OK), is marked as unhealthy

## Elastic Load Balancer Types

- [Classic Load Balancer](clb.md)
  - v1 old generation - from 2009
  - HTTP, HTTPS, TCP
- [Application Load Balancer](alb.md)
  - v2 current generation - from 2016
  - HTTP, HTTPS, WebSocket
- [Network Load Balancer](nlb.md)
  - v2 current generation - from 2017
  - TCP, TLS (secure TCP) & UDP
