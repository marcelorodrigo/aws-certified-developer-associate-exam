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

## Dynamic Scaling
Dynamics scaling policies we have four kinds:

### Target tracking scaling
- It's the most simple and easy to set up.
- Example: I want to track the average CPU utilization of my autoscaling groups across all my EC2 instances to stay at around 40%.
### Simple/Step scaling
- When a CloudWatch alarm is triggered, you add or remove EC2 machines
- Example, when CPU is above 70% you add 2. When is below 30%, you remove 1.
### Scheduled Actions
- Antecipate a scaling based on known usage patterns, based in time schedule
### Predictive Scaling
- Continously forecast load and schedule scaling ahead
- Analyzes automatically the historical load, generacate forecast using AI and scale automatically
