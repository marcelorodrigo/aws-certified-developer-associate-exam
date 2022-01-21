# Lambda
- If you increase the memory available for your lambda, you also improve CPU and network.
- Lambda to ALB conversions happen using JSON to HTTP (request and response follows a JSON format with key/values for headers, body and query parameters)
- ALB Multi-Header Values are supported
  - HTTP: `https://domain.com/path?name=Marcelo&name=Rodrigo`
  - JSON: `"queryStringParamenters: {"name": ["Marcelo","Rodrigo"]}`

## Supported Languages
- Node.js (Javascript)
- Python
- Java
- C# (.NET Core / Powershell)
- Go
- Ruby
- Custom Runtime API (Community supported, eg. Rust)
- Lambda Container Image
  - Image must implement Lambda Runtime API
  - ECS / Fargate is prefered for running Docker images
## Syncronous Invocations
- CLI, SDK, Api Gateway, Application Load Balancer
- Error handling must happen at client side (retries, exponential backoff, etc)
## Asynchronous Invocations
- S3, SNS, CloudWatch Events, etc
- Events are placed in a Event Queue (that contains DLQ)
- 2 retries for events that failed (one after 1 minute, another one 2 minutes later)

## Lambda inside your VPC
- By default any lambda runs on Amazon VPC
- To be able to access resources (such as RDS, ElastiCache, etc) you must define VPC, subnets and security groups for a lambda
- Lambda then will create an ENI (Elastic Network Interface) in your subnet, using AWSLambdaVPCAccessExecutionRole role.
- Lambda inside VPC does not have internet access (even though your EC2 machines have), you will not get access or either a public IP.
- To enable access to internet from your lambda, you need to use a NAT Gateway/Instance.

## Performance
- From 128MB to 10GB of RAM
- The more RAM you allocate, the more CPU you get
- At 1792Mb you get a full CPU
- So if you need multithreading in your lambda, more than 1792Mb is necessary
- Timeout default is 3 seconds, maximum of 900 seconds (15 minutes)

## Concurrency
- Up to 1000 concourrent executions
- It's a good practice to set concurrency limits to your lambda
- Provisioned Concurrency can be used to avoid cold start waiting times 
