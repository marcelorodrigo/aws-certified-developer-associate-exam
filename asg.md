# Auto Scaling Groups
- Scale out (add [EC2](ec2.md) instances) to match an increased load
- Sale in (remove [EC2](ec2.md) instances) to match a decreased load
- Automatically register newer instances to [ELB](elb.md)

## Auto Scaling Alarms
- It's possible to scale in/out an ASG based on CloudWatch alarms
- Custom Metric (you send metrics do CloudWatch via PutMetric API, and then you can use it as source scaling policy for ASG) 

## Scaling Policies
Metrics
- Target average CPU usage
- Requests per instance
- Network In
- Network Out

