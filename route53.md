# Route 53
## Record Types (to remember for the exam)
- A: maps a hostname to IPv4
- AAAA: maps a hostname to IPv6
- CNAME: maps a hostname to another hostname
  - Target is a domain name which must have A/AAAA record
  - Can't create CNAME for top node in a DNS namespace (Zone Apex - Root domain)
- NS: nameservers for the hosted zone

## Hosted Zones
You can have public (internet domains - example.com) and private (internal domains - example.local) hosted zones

## CNAME vs Alias
- CNAME you can point hostname to another hostname (server.mydomain.com -> other.domain.com), only works for subdomains
- Alias points hostname to an AWS Resource (works for root and sub domains)
- Free
- Native Health Check

## Routing Policies
### Simple
- Route traffic to a single resource
- Can specify multiple values in the same record, **client decides which one to connect**.
- When Alias enabled, specify only one AWS Resource
- Health Checks cannot be associated
### Weighted
- Control how much (%) requests will go to specific resource
- DNS records must have same name and type
- **Assigining 0 as weight, will stop sendind traffic to a resource**
- **But if all records are 0 as weight, then all of them will be used with same weight**
### Latency
- Redirects to resource with least latency to client
- Latency is based on traffic between client and AWS Regions
### Failover
- 
### Geolocation
### Geoproximity
### Multi Value
