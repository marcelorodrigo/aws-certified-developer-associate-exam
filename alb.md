# Application Load Balancers
- Support HTTP(S) (layer 7)
- Support HTTP/2 and WebSocket
- Load Balancing to Target Groups
- Load Balancing to multiple applications on the same EC2 (containers)
- ALB can route to multiple target groups
- Health Checks are at the target group level

## Routing Tables
- Routing based on path in URL (`example.com/users` and `example.com/admin`)
- Routing based on hostname in URL (`users.example.com` and `admin.example.com`)
- Routing based on Query String and Headers (`example.com/admin?user=123`)

## Target Groups
Possible target groups are
- EC2 Machines (possible managed by ASG) - HTTP
- EC2 Tasks (managed by ECS) - HTTP
- Lamba functions - HTTP request is translated to a JSON event
- IP Address (must be private IPs)

## Good to Know
- Fixed hostname (xxx.region.elb.amazonaws.com)
- Application cannot see real client IP address, but actually in `X-Forwarded-For` header
- Same for `X-Forwarded-Port` and `X-Forwarded-Proto`, respectively for port and protocol
