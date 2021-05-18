# EBS
- Persists data that still lives even after instance termination
- Bound to a specific Availability Zone
- Snapshots can be copied to any region
- AMI's are built to a specific region, but they can be copied across regions
- EC2 Image Builder automate the creation, maintaining, validation and testing of AMI's (and it can be scheduled)
- EC2 Local Instance Store can be used to speed up a physical disk connection to EC2 instance
- Amazon EFS (Elastic File System): is a NFS that can be mounted to several EC2 instances at once, and it costs 3x more than an EBS. It's multi AZ inside a region

## EBS Multi-Attach
- Allows a volume to be attached to multiple instances in the same AZ
- It must use a filesystem that supports cluster-aware usage
- Available only for io1 and io2 family
